<template>
  <!-- <div class="chat"> -->
  <div class="contents">
    <div class="row">
      <div class="col col-3">
        <div class="row">
          <div class="col col-12 shadow list">
            <div class="col_header">
              <h2>채팅 목록</h2>
              <span class="meta_menu delete"><a href="#">전체 삭제</a></span>
            </div>
            <div class="col_body chat_list">
              <div id="app">
                <ul v-for="post in posts" v-bind:key="post.id">
                  <li v-on:click="chat_detail(post.target_id)">
                    <div class="list_item">
                      <div class="list_top">
                        <div class="thumb">
                          <div class="thumb_img">
                            <img src="../../images/sp_mh.png">
                          </div>
                          <span class="icon_sns kt"></span>
                        </div>
                        <div class="name_wrap">
                          <div class="nickname"><span>({{post.talkType}}) </span>{{post.target_id}}</div>
                          <div class="date">{{post.timestamp}}</div>
                        </div>
                        <div class="icon_more">
                          <a href="#">
                            <img src="../../images/icon_more_h.png">
                          </a>
                        </div>
                      </div>
                      <div class="list_md">
                        <div class="talk_desc">{{post.lastMsg}} </div>
                        <span class="new_count" v-if="post.readFlag != 0">{{post.readFlag}}</span>
                      </div>
                      <div class="list_bt">
                        <span class="badge black_list">black</span>
                      </div>
                    </div>
                  </li>
                </ul>
              </div>
              <!--<button v-else v-on:click="searchTerm">글 불러오기</button>-->
            </div>
          </div>
        </div>
      </div>
      <div class="col col-9 chat_member">
        <div class="row">
          <div class="col col-5 chatting">
            <div class="col_header">
              <div class="chatting_header">
                <div class="thumb">
                  <div class="thumb_img">
                    <img src="../../images/sp_mh.png">
                  </div>
                  <span class="icon_sns kt"></span>
                </div>
                <h2>(카톡) 고객 닉네임 <span class="badge before">기존 2회</span><span class="badge book">예약중</span><span class="badge black_list">black</span></h2>
                <div class="icon_more">
                  <a href="#">
                    <img src="../../images/icon_more_h.png">
                  </a>
                </div>
              </div>
            </div>
            <div class="col_body">
              <div class="memo_section">
                <div class="memo">
                  1. 아이디 Curriculam 에서 AppleDoor로 변경되었음<br>
                  2. 2018. 12. 28 김뫄뫄 직원 1회<br>
                  3. 2019. 01. 05 김뫄뫄 직원 1회<br>
                  4. 2019. 01. 07 블랙리스트 추가<br>
                  5. 2018. 12. 28 김뫄뫄 직원 1회<br>
                  6. 2019. 01. 05 김뫄뫄 직원 1회<br>
                  7. 2019. 01. 07 블랙리스트 추가
                </div>
                <input type="text" placeholder="메모를 입력하세요.">
              </div>


              <div class="chatting_section" v-if="hasResult">
                <ul v-for="detail in details" v-bind:key="detail.idx">
                  <li>
                    <div class="message_wrap">
                      <div class="msg_txt your_log">
                        <span>{{detail.msg}}</span>
                      </div>
                      <div class="aside">{{detail.time}}</div>
                    </div>
                  </li>
                </ul>
                <div class="chatting_wrap">
                  <div class="write">
                    <textarea placeholder="보낼 메시지를 입력해 주세요.">{{this.submit_msg}}</textarea>
                  </div>
                  <button class="chat_submit" v-on:click="chat_submit()">보내기</button>
                </div>
              </div>
            </div>
          </div>
          <ChatMemberInfo></ChatMemberInfo>
        </div>
      </div>
    </div>
  </div>
  <!-- </div> -->
</template>

<script>
  import Vue from 'vue'
  import axios from 'axios'
  import ChatMemberInfo from './ChatMemberInfo'

  Vue.prototype.$http = axios
  export default {
    name: 'Chat',
    components: {
      'ChatMemberInfo': ChatMemberInfo
    },
    data: function () {
      return {
        posts: [],
        details : [],
        is_detail: false,
        target_id:-1,
        submit_msg: '',

      }
    },computed: {

    },
    mounted(){
      this.chat_list();
      this.chat_detail();

      this.interval = setInterval(function () {
        this.chat_list();
        if( this.is_detail == true ){
          this.chat_detail(this.target_id);
        }
      }.bind(this), 300);
    },
    methods: {
      hasResult: function () {
        return this.details.length > 0
      },
      // searchTerm: function () {
      //   $.get('http://13.209.76.116/chat_list.php', function (response) {
      //     // this.posts = response;
      //     console.log(response.data.data)
      //     console.log(response.data.data.chat_list)
      //     this.posts = response.data.data.chat_list
      //   }.bind(this));
      // },
      chat_list: function () {
        // using JSONPlaceholder
        const baseURI = 'http://13.209.76.116';
        this.$http.get(`${baseURI}/chat_list.php`)
        .then((result) => {
          // console.log(result.data.data)
          // console.log(result.data.data.chat_list)
          this.posts = result.data.data.chat_list
        })
      },
      chat_detail:function (target_id){
        this.is_detail = true;
        console.log(target_id);
        this.target_id = target_id;
        // using JSONPlaceholder
        const baseURI = 'http://13.209.76.116';
        this.$http.get(`${baseURI}/chat_detail.php?target_id=${target_id}`)
        .then((result) => {
          console.log(result)
          this.details = result.data.data.chat_detail;
        })
      },
      chat_submit:function(){
        //채팅 보내는 곳, api 들어와야 수정 가능

        // 보내기버튼 누르면갱신 & msg = ''
        this.chat_detail();
        this.submit_msg  = '';
      }

    },

    beforeDestroy: function(){
      clearInterval(this.interval);
    }
    // computed: {
    //   hasResult: function () {
    //     return this.posts.length > 0
    //   }
    // },
    // methods: {
    //   searchTerm: function () {
    //     // using JSONPlaceholder
    //     const baseURI = 'http://13.209.76.116';
    //     this.$http.get(`${baseURI}/chat_list.php`)
    //     .then((result) => {
    //       console.log(result.data.data)
    //       console.log(result.data.data.chat_list)
    //       this.posts = result.data.data.chat_list
    //     })
    //   }
    // }
  }
</script>

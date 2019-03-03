<template>
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
</template>

<script>
  import Vue from 'vue'
  import axios from 'axios'


  Vue.prototype.$http = axios
  export default {
    name: "ChatListItem",
    data: function () {
      return {
        posts: []
      }
    },
    mounted(){
      this.chat_list();

      this.interval = setInterval(function () {
        this.chat_list();
      }.bind(this), 300);
    },
    methods: {
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
          console.log(result.data.data)
          console.log(result.data.data.chat_list)
          this.posts = result.data.data.chat_list
        })
      },
      chat_detail:function (target_id){

        console.log(target_id)
        // using JSONPlaceholder
        const baseURI = 'http://13.209.76.116';
        this.$http.get(`${baseURI}/chat_detail.php?target_id=${target_id}`)
        .then((result) => {
          console.log(result)
        })
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

<style scoped>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    max-width: 560px;
  }
</style>

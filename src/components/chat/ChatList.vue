<template>
  <div class="col col-12 shadow list">
    <div class="col_header">
      <h2>채팅 목록</h2>
      <span class="meta_menu delete"><a href="#">전체 삭제</a></span>
    </div>
    <div class="col_body chat_list">
      <ul>
        <li class="active">
          <div class="list_item">
            <div class="list_top">
              <div class="thumb">
                <div class="thumb_img">
                  <img src="../../images/sp_mh.png">
                </div>
                <span class="icon_sns kt"></span>
              </div>
              <div class="name_wrap">
                <div class="nickname"><span>(카톡) </span>고객 닉네임</div>
                <div class="date">오후 2:20</div>
              </div>
              <div class="icon_more">
                <a href="#">
                  <img src="../../images/icon_more_h.png">
                </a>
              </div>
            </div>
            <div class="list_md">
              <div class="talk_desc">블랙리스트 풀어주세요.</div>
            </div>
            <div class="list_bt">
              <span class="badge before">기존 2회</span><span class="badge book">예약중</span><span class="badge black_list">black</span>
            </div>
          </div>
        </li>
        <li>
          <div class="list_item">
            <div class="list_top">
              <div class="thumb">
                <div class="thumb_img">
                  <img src="../../images/thumb_default.png">
                </div>
                <span class="icon_sns kt"></span>
              </div>
              <div class="name_wrap">
                <div class="nickname"><span>(카톡) </span>닉네임</div>
                <div class="date">어제</div>
              </div>
              <div class="icon_more">
                <a href="#">
                  <img src="../../images/icon_more_h.png">
                </a>
              </div>
            </div>
            <div class="list_md">
              <div class="talk_desc">안녕하세요. </div>
              <span class="new_count">6</span>
            </div>
            <div class="list_bt">
              <span class="badge black_list">black</span>
            </div>
          </div>
        </li>
        <li>
          <div class="list_item">
            <div class="list_top">
              <div class="thumb">
                <div class="thumb_img">
                  <img src="../../images/thumb_default.png">
                </div>
                <span class="icon_sns kt"></span>
              </div>
              <div class="name_wrap">
                <div class="nickname"><span>(카톡) </span>고객쓰</div>
                <div class="date">1월 16일</div>
              </div>
              <div class="icon_more">
                <a href="#">
                  <img src="../../images/icon_more_h.png">
                </a>
              </div>
            </div>
            <div class="list_md">
              <div class="talk_desc">안녕하세요. </div>
              <span class="new_count">6</span>
            </div>
            <div class="list_bt">

            </div>
          </div>
        </li>
        <li>
          <div class="list_item">
            <div class="list_top">
              <div class="thumb">
                <div class="thumb_img">
                  <img src="../../images/thumb_default.png">
                </div>
                <span class="icon_sns kt"></span>
              </div>
              <div class="name_wrap">
                <div class="nickname"><span>(카톡) </span>손님</div>
                <div class="date">1월 15일</div>
              </div>
              <div class="icon_more">
                <a href="#">
                  <img src="../../images/icon_more_h.png">
                </a>
              </div>
            </div>
            <div class="list_md">
              <div class="talk_desc">안녕하세요. 커리큘럼 커리큘럼 커리큘럼</div>
            </div>
            <div class="list_bt">
              <span class="badge before">기존 2회</span><span class="badge book">예약중</span>
            </div>
          </div>
        </li>
        <li>
          <div class="list_item">
            <div class="list_top">
              <div class="thumb">
                <div class="thumb_img">
                  <img src="../../images/thumb_default.png">
                </div>
                <span class="icon_sns kt"></span>
              </div>
              <div class="name_wrap">
                <div class="nickname"><span>(카톡) </span>고객 닉네임</div>
                <div class="date">2018.12.30</div>
              </div>
              <div class="icon_more">
                <a href="#">
                  <img src="../../images/icon_more_h.png">
                </a>
              </div>
            </div>
            <div class="list_md">
              <div class="talk_desc">안녕하세요를레이히 </div>
            </div>
            <div class="list_bt">

            </div>
          </div>
        </li>
        <li>
          <div class="list_item">
            <div class="list_top">
              <div class="thumb">
                <div class="thumb_img">
                  <img src="../../images/sp_mh.png">
                </div>
                <span class="icon_sns kt"></span>
              </div>
              <div class="name_wrap">
                <div class="nickname"><span>(카톡) </span>고객 닉네임</div>
                <div class="date">2018.12.30</div>
              </div>
              <div class="icon_more">
                <a href="#">
                  <img src="../../images/icon_more_h.png">
                </a>
              </div>
            </div>
            <div class="list_md">
              <div class="talk_desc">안녕하세요. 동해물과 백두산이 마르고 닳도록 하느님이 보우하사 우리나라 만세 무궁화 삼천리 화려강산 대한사랑 대한으로 길이 보전하세.</div>
            </div>
            <div class="list_bt">
              <span class="badge before">기존 2회</span><span class="badge book">예약중</span><span class="badge black_list">black</span>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'ChatList'
  }
</script>


<template>
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
      <div class="chatting_section">
        <div class="message_wrap">
          <div class="msg_txt your_log">
            <span>안녕하세요. 동해물과 백두산이 마르고</span>
          </div>
          <div class="aside">오전 10:30</div>
        </div>
        <div class="message_wrap">
          <div class="msg_txt my_log">
            <span>안녕하세요. 동해물과 백두산이 마르고 안녕하세요. 동해물과 백두산이 마르고 닳도록 하느님이 보우하사 우리나라만세. 무궁화 삼천리 화려강산, 대한 사람 대한으로 길이 보전하세. 남산 위에 저 소나무 철갑을 두른 듯. </span>
          </div>
          <div class="aside">오전 10:30</div>
        </div>
        <div class="chatting_wrap">
          <div class="write">
            <textarea placeholder="보낼 메시지를 입력해 주세요."></textarea>
          </div>
          <button class="chat_submit">보내기</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'ChatForm'
  }
</script>

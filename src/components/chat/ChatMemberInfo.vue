<template>
  <div class="col col-7 member">
    <div class="col_header center">
      <h2>직원 정보</h2>
    </div>
    <div class="row">
      <div class="col col-6 chat_member_info">
        <div class="chat_profile">
          <div class="profile">
            <div class="name">김직원</div>
            <div class="locate">25살 여, 부산 서면 롯데백화점</div>
            <div class="sns">
              <div class="sns_item kakao">
                <img src="../../images/profile_kt.png"><span class="sns_id kt_id">kakaoid</span>
              </div>
              <div class="sns_item line">
                <img src="../../images/profile_line.png"><span class="sns_id kt_id">lineid</span>
              </div>
              <div class="sns_item tele">
                <img src="../../images/profile_tele.png"><span class="sns_id kt_id">teleid</span>
              </div>
            </div>
            <div class="priv_memo">
              <div class="memo">
                <div class="shortcut">
                  <span class="ctrl_key">Ctrl +</span> <div class="ctrl_number"><span>1</span></div>
                </div>
                <div class="memo_txt">
                  안녕하세요, 반갑습니다.
                </div>
              </div>
              <div class="memo">
                <div class="shortcut">
                  <span class="ctrl_key">Ctrl +</span> <div class="ctrl_number"><span>2</span></div>
                </div>
                <div class="memo_txt">
                  어쩌면 누군가를 사랑하는 것보다 더 어려운 게 나 자신을 사랑하는 것.
                </div>
              </div>
              <div class="memo">
                <div class="shortcut">
                  <span class="ctrl_key">Ctrl +</span> <div class="ctrl_number"><span>3</span></div>
                </div>
                <div class="memo_txt">
                  차가운 밤의 시선 초라한 날 감추려 몹시 뒤척였지만, 저 수많은 별을 맞기 위해 난 떨어졌던가. 저 수천개의 찬란한 화살.
                </div>
              </div>
              <div class="memo">
                <div class="shortcut">
                  <span class="ctrl_key">Ctrl +</span> <div class="ctrl_number"><span>4</span></div>
                </div>
                <div class="memo_txt">
                  안녕하세요, 반갑습니다.
                </div>
              </div>
              <div class="memo">
                <div class="shortcut">
                  <span class="ctrl_key">Ctrl +</span> <div class="ctrl_number"><span>5</span></div>
                </div>
                <div class="memo_txt">
                  어쩌면 누군가를 사랑하는 것보다 더 어려운 게 나 자신을 사랑하는 것.
                </div>
              </div>
              <div class="memo">
                <div class="shortcut">
                  <span class="ctrl_key">Ctrl +</span> <div class="ctrl_number"><span>6</span></div>
                </div>
                <div class="memo_txt">
                  차가운 밤의 시선 초라한 날 감추려 몹시 뒤척였지만, 저 수많은 별을 맞기 위해 난 떨어졌던가. 저 수천개의 찬란한 화살.
                </div>
              </div>
              <div class="memo">
                <div class="shortcut">
                  <span class="ctrl_key">Ctrl +</span> <div class="ctrl_number"><span>7</span></div>
                </div>
                <div class="memo_txt">
                  안녕하세요, 반갑습니다.
                </div>
              </div>
              <div class="memo">
                <div class="shortcut">
                  <span class="ctrl_key">Ctrl +</span> <div class="ctrl_number"><span>8</span></div>
                </div>
                <div class="memo_txt">
                  어쩌면 누군가를 사랑하는 것보다 더 어려운 게 나 자신을 사랑하는 것.
                </div>
              </div>
              <div class="memo">
                <div class="shortcut">
                  <span class="ctrl_key">Ctrl +</span> <div class="ctrl_number"><span>9</span></div>
                </div>
                <div class="memo_txt">
                  차가운 밤의 시선 초라한 날 감추려 몹시 뒤척였지만, 저 수많은 별을 맞기 위해 난 떨어졌던가. 저 수천개의 찬란한 화살.
                </div>
              </div>
              <div class="memo">
                <div class="shortcut">
                  <span class="ctrl_key">Ctrl +</span> <div class="ctrl_number"><span>0</span></div>
                </div>
                <div class="memo_txt">
                  차가운 밤의 시선 초라한 날 감추려 몹시 뒤척였지만, 저 수많은 별을 맞기 위해 난 떨어졌던가. 저 수천개의 찬란한 화살.
                </div>
              </div>
              <div class="memo">
                <div class="row">
                  <div class="col col-4">
                    <div class="shortcut">
                      <span class="ctrl_key">Alt +</span> <div class="alt_number"><span>1</span></div>
                    </div>
                    <div class="memo_img">
                      <img src="../../images/sample02.jpg">
                    </div>
                  </div>
                  <div class="col col-4">
                    <div class="shortcut">
                      <span class="ctrl_key">Alt +</span> <div class="alt_number"><span>2</span></div>
                    </div>
                    <div class="memo_img">
                      <img src="../../images/sample02.jpg">
                    </div>
                  </div>
                  <div class="col col-4">
                    <div class="shortcut">
                      <span class="ctrl_key">Alt +</span> <div class="alt_number"><span>3</span></div>
                    </div>
                    <div class="memo_img">
                      <img src="../../images/sample02.jpg">
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col col-6 schedule_info">
        <Schedule></Schedule>
      </div>
    </div>
  </div>
</template>

<script>
  import Schedule from './Schedule'

  export default {
    name: 'ChatMemberInfo',
    components: {
      'Schedule': Schedule,
    }
  }
</script>

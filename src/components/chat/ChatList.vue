<template>
  <div class="col col-12 shadow list">
    <div class="col_header">
      <h2>채팅 목록</h2>
      <span class="meta_menu delete"><a href="#">전체 삭제</a></span>
    </div>
   <ChatListItem></ChatListItem>
  </div>
</template>


<script>
  import ChatListItem from './ChatListItem'
  export default {
    name: 'ChatList',
    components: {
      'ChatListItem': ChatListItem,
    }
  }
</script>


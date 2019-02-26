<template>
  <!-- <div class="chat"> -->
  <div class="contents">
    <div class="row">
      <div class="col col-3">
        <div class="row">
          <ChatList></ChatList>
        </div>
      </div>
      <div class="col col-9 chat_member">
        <div class="row">
          <ChatForm></ChatForm>
          <ChatMemberInfo></ChatMemberInfo>
        </div>
      </div>
    </div>
  </div>
  <!-- </div> -->
</template>

<script>
  import ChatList from './ChatList'
  import ChatForm from './ChatForm'
  import ChatMemberInfo from './ChatMemberInfo'

  export default {
    name: 'Chat',
    components: {
      'ChatList': ChatList,
      'ChatForm': ChatForm,
      'ChatMemberInfo': ChatMemberInfo
    }
  }
</script>

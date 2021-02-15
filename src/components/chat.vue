<template>
  <div class="chat">
    <div class="menu">
      <div class="nickname">@ Nurbakhyt</div>
      <div class="call">
        <span class="phone"
          ><img src="../assets/images/call-phone.svg" alt="call-phone"
        /></span>
        <span class="video"
          ><img src="../assets/images/video.svg" alt="video"
        /></span>
        <span class="fixed-m"
          ><img src="../assets/images/pin.svg" alt="pin"
        /></span>
        <span class="add-friend"
          ><img src="../assets/images/user-add.svg" alt="user-add"
        /></span>

        <input type="text" placeholder="Поиск" />
        <div class="helper">
          <span class="post"
            ><img src="../assets/images/post.svg" alt="post"
          /></span>
          <span class="help"
            ><img class="help-img" src="../assets/images/help.svg" alt="help"
          /></span>
        </div>
      </div>
    </div>
    <messagetext />
  </div>
  
  <chatter />
</template>

<script>
import chatter from "./chatter.vue";
import messagetext from "./messagetext.vue";

export default {
  data() {
    return {};
  },
  components: {
    chatter,
    messagetext,
  },
};
</script>

<style scoped>
* {
  box-sizing: border-box;
}
.chat {
  min-height: 100vh;
  max-height: 100vh;
  height: 100%;
  min-width: 100vw;
  width: 100%;
  display: flex;
  flex-direction: column;

  background-color: #333;
}
.menu {
  height: 52px;
  display: flex;
  justify-content: space-between;
  padding: 10px;
  max-width: 85vw;
  width: 100vw;
  margin-top: 10px;
  border-bottom: 1px solid #fff;
}
.nickname {
  font-size: 18px;
  line-height: 20px;
  color: #fff;
}
.call {
  display: flex;
  justify-content: space-between;
}
span {
  cursor: pointer;
}
span + span {
  margin-left: 20px;
}
input {
  width: 150px;
  height: 30px;
  border: 1px solid transparent;
  border-radius: 4px;
  margin: 0 30px;
}
.helper {
  flex: none;
  margin-right: 50px;
}
.help {
  margin-right: 30px;
}
</style>
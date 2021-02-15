<template>
  <div class="settings">
    <div class="nick-details">
      <div class="nick">
        {{ nick }}
      </div>
      <div class="number">{{ number }}</div>
    </div>
    <div class="panel">
      <span class="microphone"><img src="../assets/images/microphone.svg" alt="microphone"></span>
      <span class="headphone"><img src="../assets/images/headphones.svg" alt="headphone"></span>
      <span class="settings-acc"><img src="../assets/images/settings.svg" alt="settings"></span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nick: "Whojesus",
      number: "#7130",
    };
  },
  components: {},
  methods: {},
};
</script>

<style scoped>
* {
  box-sizing: border-box;
}
.settings {
  background-color: rgba(17, 24, 39, 1);
  border-top: 1px solid rgba(17, 24, 39, 1);
  display: grid;
  grid-column: 50% 50%;
  height: 50px;
  width: 225px;
  margin: 0;
  padding: 5px;
  position: absolute;
  left: 0;
  bottom: 0;
  position: fixed;
  margin-left: 8px;
}
.nick-details {
  display: flex;
  flex-direction: column;
  position: absolute;
  left: 50px;
  top: 10px;
  color: #fff;
}
.nick-details::before {
  content: url("../assets/images/discord.svg");
  position: absolute;
  left: 0;
  object-fit: cover;
  position: absolute;
  left: -40px;
  bottom: 0px;
}
.panel{
    position: absolute;
    right: 25px;
    top: 20px;
}
span{
    cursor: pointer;
    width: 30px;
    height: 30px;
}
span + span {
    margin-left: 10px;
}
</style>
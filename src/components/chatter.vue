<template>
  <div class="chatter">
    <label for="text">
      <input type="text" placeholder="Написать @Nurbakyt" />
      <button class="add-file">+</button>
      <div class="btns">
        <button class="box"></button>
        <button class="gif"></button>
        <button class="smile"></button>
      </div>
    </label>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style scoped>
.chatter {
  position: absolute;
  bottom: 25px;
  left: 250px;
  display: flex;
}
label {
  min-width: 750px;
  max-width: 1500px;
  display: flex;
  position: relative;
  background-color: #333;
}

input {
  width: 100%;
  margin-right: 20px;
  min-width: 750px;
  border: 1px solid transparent;
  border-radius: 4px;
  height: 50px;
  padding-left: 75px;
  padding-right: 150px;
  background-color: #9f9b9b;
  color: #000;
}
@media (min-width: 1050px) and (max-width: 1200px) {
  label {
    width: 800px;
  }
}
@media (min-width: 1200px) and (max-width: 1500px){
  label {
    width: 950px;
  }
}
@media (min-width: 1500px){
  label {
    width: 1200px;
  }
}
.add-file {
  cursor: pointer;
  position: absolute;
  top: 10px;
  left: 15px;
  background-color: #303132;
  border: 1px solid transparent;
  border-radius: 100%;
  font-size: 22px;
}
.add-file:hover {
  background-color: #3f3f3f;
}
.btns{
    
    display: flex;
    justify-content: space-between;
    width: 120px;
    position: absolute;
    right: 35px;
    top: 10px;
}
.btns button{
    height: 30px;
    width: 30px;
    cursor: pointer;
    background-color: #303132;
}

.box{
    background-image: url("../assets/images/box.svg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
}
.gif{
    background-image: url("../assets/images/gif.svg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
}
.smile{
    background-image: url("../assets/images/smile.svg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
}
</style>
<template>
  <div>

    <navigation/>
    <chat/>
    
    

  
  </div>
</template>

<script>
// @ is an alias to /src
import navigation from "@/components/navigation.vue";
import chat from "@/components/chat.vue";

export default {
  name: "discord",
  components: {
    navigation,
    chat
    
  },
};
</script>

<style scoped>
div {
  display: flex;
  

}
</style>


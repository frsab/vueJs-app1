<template lang="html">
  <section class="message">
    <h1>message Component</h1>
    <h1>{{messageData}}</h1>
    <appInput :msg="messageData" @messageChanged="messageData= $event"></appInput>
  </section>
</template>

<script lang="js">
  import appInput from "./input.vue";
  export default  {
    name: 'message',
    data() {
      return {
        messageData :'un message de composant message ! '
      }
    },
    components:{
      appInput
    }
}
</script>

<style scoped lang="scss">
  .message {

  }
</style>

<template lang="html">

  <section class="input">
    <h1>input Component</h1>
    <input type="text" :value="msg" @input="changeMessage">
    <button  @click="init">init</button>
    <button  @click="modifierParent"> modifier prop1 de parent</button>
<!--     <input type="text" v-bind:value="msg">-->
    {{message}}
  </section>

</template>

<script lang="js">
  export default  {
    name: 'appInput',
    props: ['msg'],
    mounted() {

    },
    data() {
      return {
        message:''

      }
    },
    methods: {
      modifierParent: function(){
        this.$emit('ordreModifierParent','child proposition');
      },
      changeMessage: function (event) {
        this.message= event.target.value;
        this.$emit('messageChanged',this.message);
      }
    },
    computed: {

    }
}
</script>

<style scoped lang="scss">
  .input {

  }
</style>

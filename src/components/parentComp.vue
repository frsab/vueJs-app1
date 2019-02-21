<template lang="html">

  <section class="parent-comp">

    <message></message>
  </section>

</template>

<script lang="js">
  import appInput from "./input.vue";
  import Message from "./message";

  export default  {
    name: 'parent-comp',
    props: [],
    components: {
      Message,
      appInput
    },
    mounted() {

    },
    data() {
      return {

      }
    },
    methods: {

    },
    computed: {

    }
}
</script>

<style scoped lang="scss">
  .parent-comp {

  }
</style>

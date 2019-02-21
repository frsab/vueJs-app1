<template lang="html">

  <section class="my-component">
    <h1>my-component Component</h1>
  </section>

</template>

<script lang="js">
  export default  {
    name: 'MyComponent',
    props: [
            'prop1'
    ],
    mounted() {

    },
    data() {
      return {

      }
    },
    methods: {

      fireEvent() {
        this.$emit('myEvent', eventValueOne, eventValueTwo);
      }

    },
    computed: {

    }
}
</script>

<style scoped lang="scss">
  .my-component {

  }
</style>

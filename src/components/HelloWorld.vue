<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <my-component></my-component>

    <my-component v-bind:prop1="parentValue"></my-component>
    <!-- Or more succinctly, -->
    <my-component :prop1="parentValue"></my-component>

    <my-component v-on:click="parentHandler"></my-component>
    <!-- Or more succinctly, -->
    <my-component @myEvent="parentHandler"></my-component>
  </div>
</template>

<script>
  import MyComponent from './myComponent.vue'

export default {
  name: 'HelloWorld',
  components: {
    MyComponent
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

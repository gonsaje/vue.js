<template>
  <Example title="TEST COMPONENT" />
</template>

<script>
import ExampleVue from "./components/Example.vue";
export default {
  name: "App",
  components: {
    Example: ExampleVue,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

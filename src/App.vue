<template>
  <TheHome name="Diego" last-name="Reyes" otro="algo" />
</template>

<script>
import TheHome from "./components/TheHome.vue";
import { provide } from "vue";

export default {
  name: "App",
  components: {
    TheHome,
  },
  setup() {
    provide("username", "yeyodev");
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

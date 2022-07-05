<template>
  <div>
    <TheModal />
  </div>
</template>

<script>
import TheModal from "./components/TheModal.vue";
export default {
  name: "App",
  components: { TheModal },
  data: () => ({}),
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

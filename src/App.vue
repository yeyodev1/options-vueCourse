<template>
  <div>
    {{ text }}
  </div>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    text: "Hola vue",
  }),

  beforeCreate() {
    console.log("beforeCreate", this.$data, this.$el);
  },
  created() {
    console.log("Created", this.$data, this.$el);
  },
  mounted() {
    console.log("mounted", this.$data, this.$el);
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

<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->

    <SlotExample :msg="msg">
      <h2 slot="lineOne">
        (slots, binding HTML classes, conditional rendering, props)
      </h2>
    </SlotExample>

    <Tabs></Tabs>
  </div>
</template>

<script>
  import SlotExample from "./components/SlotExample.vue";
  import Tabs from "./components/Tabs.vue";

  export default {
    name: "app",
    components: {
      SlotExample,
      Tabs
    },
    data() {
      return {
        msg: "Vue.js Tabs Tutorial"
      };
    }
  };
</script>

<style>
  #app {
    /*font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;*/
    text-align: center;
  }
  #app h2 {
    color: #111;
  }
</style>

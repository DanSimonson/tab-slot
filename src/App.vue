<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!--
      <SlotExample :msg="msg">
        <h2 slot="lineOne">parent message one to child who shows the message</h2>
        <h2 slot="lineTwo">parent message Two to child who shows the message</h2>
      </SlotExample>
    -->
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
        msg: "messages from parent to child who shows the message"
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
  }
</style>

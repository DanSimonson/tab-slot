<template>
  <div class="Tabs">
    <!--
      <h1>{{ msg }}</h1>
      Child One<br />
      <slot name="lineOne"></slot> Child Two <br />
      <slot name="lineTwo"></slot>
    -->
    <div class="myButtonDiv">
      <button
        v-for="(tab,index) in tabs"
        :class="{active : currentTab === index }"
        @click="currentTab = index"
      >
        {{ tab }}
      </button>
    </div>
    <div class="tab-content">
      <div v-show="currentTab === 0"><h1>Tab1 content</h1></div>
      <div v-show="currentTab === 1"><h1>Tab2 content</h1></div>
      <div v-show="currentTab === 2"><h1>Tab3 content</h1></div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Tabs",
    props: {
      msg: String
    },
    data() {
      return {
        currentTab: 0,
        tabs: ["Funny Dog", "Funny Cat", "Funny ?"]
      };
    }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .tabs {
  }
  .myButtonDiv {
    border: 5px solid red;

    padding: 30px;
    width: 60%;
    margin: 0 auto;
  }
  div.myButtonDiv {
    border: 5px solid black;
    display: flex;
    justify-content: flex-start;
    padding-top: 100px;
    padding-bottom: 0;

    /*padding-top: 100px;
    padding-bottom: 0;
    padding-right: 200px;*/
  }
  button {
    padding: 10px 30px;
    margin-right: 5px;
  }
  button.active {
    background-color: lightgreen;
  }
  .tab-content {
    padding: 30px;
    border: 1px solid #ccc;
    width: 60%;
    margin: 0 auto;
    text-align: center;
  }
</style>

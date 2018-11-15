<template>
  <div class="Tabs">
    <div class="wrapper">
      <div class="myOuterDiv">
        <div
          class="innerDiv"
          v-for="(tab,index) in tabs"
          :class="{active : currentTab === index }"
          @click="currentTab = index"
        >
          {{ tab }}
        </div>
      </div>
    </div>
    <div class="tab-content">
      <div v-show="currentTab === 0">
        <video controls>
          <source src="https://i.imgur.com/8Rq54oO.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
      </div>

      <div v-show="currentTab === 1">
        <video controls>
          <source src="https://i.imgur.com/FT22P3z.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
      </div>
      <div v-show="currentTab === 2">
        <video controls>
          <source src="https://i.imgur.com/H0YtUvw.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
      </div>
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
        tabs: ["Funny Dog", "Funny Cat", "Funny Homer"]
      };
    }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  video {
    width: 100%;
    height: 300px;
  }
  .wrapper {
    /*border: 5px solid orange;*/
    width: 60%;
    margin: 0 auto;
    /*padding: 30px;
    border: 1px solid #ccc;    
    ;*/
  }

  .myOuterDiv {
    display: flex;
    justify-content: flex-start;
    background-color: #eeeeee;
  }
  .innerDiv {
    margin-right: 5px;
    /*border: 2px solid #333;*/
    padding: 5px;
  }
  .innerDiv.active {
    background-color: whitesmoke;
    border-left: 2px solid #bdbdbd;
    border-top: 2px solid #bdbdbd;
    border-right: 2px solid #bdbdbd;
  }
  .innerDiv:hover {
    cursor: pointer;
  }

  .tab-content div {
    padding: 30px;
    border: 2px solid #bdbdbd;
    border-top: 2px solid #bdbdbd;
    width: 60%;
    margin: 0 auto;
    animation: fadeEffect 1s; /* Fading effect takes 1 second */
  }
  @keyframes fadeEffect {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }
</style>

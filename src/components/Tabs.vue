<template>
  <div class="Tabs">
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
      <div v-show="currentTab === 0">
        <video controls>
          <source src="https://i.imgur.com/8Rq54oO.mp4" type="video/mp4" />
          <!-- <source src="movie.ogg" type="video/ogg" /> -->
          Your browser does not support the video tag.
        </video>
      </div>

      <div v-show="currentTab === 1">
        <video controls>
          <source src="https://i.imgur.com/FT22P3z.mp4" type="video/mp4" />
          <!-- <source src="movie.ogg" type="video/ogg" /> -->
          Your browser does not support the video tag.
        </video>
      </div>
      <div v-show="currentTab === 2">
        <video controls>
          <source src="https://i.imgur.com/H0YtUvw.mp4" type="video/mp4" />
          <!-- <source src="movie.ogg" type="video/ogg" /> -->
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
  button {
    padding: 10px;
    margin-right: 5px;
    color: #111;
  }
  button.active {
    background-color: lightgreen;
  }
  .tab-content div {
    padding: 30px;
    border: 1px solid #ccc;
    width: 60%;
    margin: 0 auto;
  }
</style>

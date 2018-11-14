<template>
  <div class="mySlots">
    <h1>{{ msg }}</h1>
    <slot name="lineOne"></slot>
  </div>
</template>

<script>
  export default {
    name: "SlotExample",
    props: {
      msg: String
    }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .mySlots {
    display: flex;
    flex-direction: column;
    color: #111;
  }

  h1 {
    margin: 40px 0 0;
    color: #333;
  }
</style>

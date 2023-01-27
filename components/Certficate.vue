<template>
  <div class="certficate">
    <h3>{{ name }}</h3>
  </div>
</template>

<script>
export default {
  name: "Certficate",
  props: {
    name: String,
    origin: String,
    photo: String,
    workIcon: String,
    color: String,
    backgroundColor: String,
  },
  
}
</script>

<style scoped>
  .certficate {
    width: 280px;
    height: 420px;

    margin-left: 1%;
    margin-right: 1%;

    border-radius: 1vh;
    border: 1vh solid #8257E5;
    box-shadow: 0 0 4px 0 #00000025;

    background-color: #0D0D0D;

    color: #fff;
  }
</style>
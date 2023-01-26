<template>
  <div class="container">
    <UserCard/>
  </div>
</template>

<script>
  import UserCard from "@/components/UserCard.vue"

  export default {
    components:{
      UserCard
    }
  }
</script>

<style>
  * {
    margin: 0;
    padding: 0;
  }
  .container {
    display: flex;
    flex-direction: column;

    width: 100vw;
    height: 100vh;

    background-color: #181818;
  }
</style>
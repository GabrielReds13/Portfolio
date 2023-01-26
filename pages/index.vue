<template>
  <div class="container">
    <div class="homeCards">
      <UserCard/>
      <SkillsCard/>
    </div>
  </div>
</template>

<script>
  import UserCard from "@/components/UserCard.vue"
  import SkillsCard from "@/components/SkillsCard.vue"

  export default {
    components:{
      UserCard,
      SkillsCard
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
  .homeCards {
    display: flex;
    flex-direction: row;

    justify-content: space-around;
  }
</style>
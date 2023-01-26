<template>
  <div class="container">
    <div class="homeCards">
      <UserCard/>
      <SkillsCard/>
      <AchivimentsCard/>
    </div>
  </div>
</template>

<script>
  import UserCard from "@/components/UserCard.vue"
  import SkillsCard from "@/components/SkillsCard.vue"
  import AchivimentsCard from "@/components/AchivimentsCard.vue"

  export default {
    components:{
      UserCard,
      SkillsCard,
      AchivimentsCard
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

    justify-content: space-evenly;
  }
</style>
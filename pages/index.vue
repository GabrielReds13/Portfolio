<template>
  <div class="container">
    <!-- Head page -->
    <head>
      <title>GabrielReds13 - Home</title>
    </head>

    <!-- Content page -->
    <div class="backgroundProfile"></div>
    <div class="homeCards">
      <UserCard/>
      <SkillsCard/>
      <AchivimentsCard/>
    </div>

    <CertficateCard/>
  </div>
</template>

<script>
  import UserCard from "@/components/UserCard.vue"
  import SkillsCard from "@/components/SkillsCard.vue"
  import AchivimentsCard from "@/components/AchivimentsCard.vue"
  import CertficateCard from "@/components/CertficateCard.vue"

  export default {
    components:{
      UserCard,
      SkillsCard,
      AchivimentsCard,
      CertficateCard
    }
  }
</script>

<style scoped>
  * {
    margin: 0;
    padding: 0;
  }
  .container {
    display: flex;
    flex-direction: column;
    align-items: center;

    width: 100vw;
    height: 280vh !important;

    background-color: #181818;
  }

  /* Backgrond photo */
  .backgroundProfile {
    width: 100vw;
    height: 25vh;

    background-image: url("@/assets/BackgrounPhoto.jpg");
    background-repeat: repeat;
    background-position: center left;
  }

  /* Home */
  .homeCards {
    display: flex;
    flex-direction: row;
    width: 100vw;

    margin-top: 5%;

    justify-content: space-evenly;

    position: absolute;
    z-index: 3;
  }
</style>
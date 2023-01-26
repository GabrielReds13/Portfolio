<template>
  <div class="skillsCard Card">
    <div class="HeaderCard">
      <h3>Skills:</h3>
    </div>
    <!-- Skills -->
    <div class="scrollSkills">
      <!-- Skill Card -->
      <Skill/>
      <Skill/>
      <Skill/>
      <Skill/>
      <Skill/>
      <Skill/>
      <Skill/>
    </div>
  </div>
</template>

<script>
  import Skill from "./Skill.vue"
  export default {
    name: "SkillsCard",
    components: {
      Skill
    }
  }
</script>

<style scoped>
  .skillsCard {
    width: 30vw !important;
  }
  .scrollSkills {
    display: flex;
    flex-direction: column;

    width: 100%;  
    height: 100%;

    justify-content: initial;
    align-items: center;
    overflow-x: hidden;
    overflow-y: scroll;
  }

  ::-webkit-scrollbar {
    width: 5px;
  }
  ::-webkit-scrollbar-thumb {
    background: #fff;
    border-radius: 90px;
  }
  ::-webkit-scrollbar-track {
    background: #1A1A1A;
  }
</style>
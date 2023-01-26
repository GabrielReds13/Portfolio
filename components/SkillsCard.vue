<template>
  <div class="skillsCard Card">
    <div class="HeaderCard">
      <h3>Skills:</h3>
    </div>
    <!-- Skills -->
    <div class="scrollSkills">
      <!-- Skill Card -->
      <div class="skillCard">
        <!-- Skill Infos -->
        <div class="infoSkill">
          <!-- Skill Icon -->
          <img src="@/assets/SkillsIcons/VueLogo.svg" alt="VueJS">
          <!-- Skill Status -->
          <div class="skillStatus">
            <h3 class="skillName">VueJS</h3>
            <div class="dividerSkill"></div>
            <!-- Status -->
            <ul class="status">
              <li class="levelSkill">
                <img src="" alt=""> 
                <p class=""></p>
              </li>
              <li class="progressSkill">
                <img src="" alt=""> 
                <p class=""></p>
              </li>
              <li class="achivimentsSkill">
                <img src="" alt=""> 
                <p class=""></p>
              </li>
            </ul>
          </div>
        </div>
          
        <!-- Progress Bar -->
        <div class="progressBar"><div id="percentageProgress"></div></div>
      </div>
    </div>
  </div>
</template>

<script>
  import "@/styles/SkillCardStyle.css"

  export default {
    name: "SkillsCard",
  }
</script>

<style scoped>
  .scrollSkills {
    display: flex;
    flex-direction: column;

    width: 100%;  
    height: 100%;

    justify-content: initial;
    align-items: center;
    overflow: auto;
  }
</style>
<template>
  <div class="skillCard">
    <!-- Content -->
    <div class="contentSkillCard">

      <!-- Skill Infos -->
      <div class="infoSkill">
        <!-- Skill Icon -->
        <img class="skillLogo" src="@/assets/SkillsIcons/VueLogo.svg" alt="VueJS">

        <!-- Skill Status -->
        <div class="skillStatus">
          <h3 class="skillName">VueJS</h3>
          <div class="dividerSkill"></div>
          <!-- Status -->
          <ul class="status">
            <li class="levelSkill">
              <img src="@/assets/icons/StarLevel.svg" alt="Estrela"> 
              <p class="">Nível: </p>
            </li>
            <li class="progressSkill">
              <img src="@/assets/icons/ArrowLevel.svg" alt="Seta de nível"> 
              <p class="">Progresso: </p>
            </li>
            <li class="achivimentsSkill">
              <img src="@/assets/icons/Trophy.svg" alt="Troféu"> 
              <p class="">Conquistas: 50 de 50</p>
            </li>
          </ul>
        </div>
      </div>

    </div>
      
    <!-- Progress Bar -->
    <div class="progressBar"><div id="percentageProgress"></div></div>
  </div>
</template>

<script>
export default {
  name: "Skill"
}
</script>

<style scoped>
.skillCard {
  display: flex;
  flex-direction: column;

  justify-content: space-between;

  width: 90%;
  min-height: 150px !important;
  height: 33%;

  border-radius: 2%;

  background-color: #00000025;
  box-shadow: 0 0 4px 0 #00000025;

  margin-top: 5%;
  margin-bottom: 2%;
}
.contentSkillCard {
  display: flex;

  width: 100%;
  height: 95%;
  
  align-items: center;
  
}

/* Skill Info */
.infoSkill {
  display: flex;
  flex-direction: row;
  
  width: 100%;

  justify-content: space-around;
  align-items: center;

  transform: translateX(2%);
  margin-top: 2%;
}
.skillLogo {
  display: flex;
  
  width: 12vh;
  height: 12vh;
}

.skillStatus {
  display: flex;
  flex-direction: column;
  
  width: 60%;
}

.dividerSkill {
  width: 30%;
  height: 0.3vh;

  border-radius: 999px;
  margin-top: 2%;
  margin-bottom: 5%;
  background-color: #fff;
}

/* Status */
.status {
  display: flex;
  flex-direction: column;
  list-style: none;
  color: #C4C4C4;
}
.status li {
  display: flex;
  flex-direction: row;
}
.progressSkill,
.levelSkill {
  margin-left: 1%;
}
.status li p {
  margin-left: 5%;
}
.progressSkill p {
  margin-left: 7% !important;
}
.levelSkill p {
  margin-left: 8.5% !important;
}

/* Progress Bar */
.progressBar {
  width: 100%;
  height: 5%;

  background-color: #1A1A1A;
}
#percentageProgress {
  width: 25%;
  height: 100%;

  background-color: #fff;
}
</style>
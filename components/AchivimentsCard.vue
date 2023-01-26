<template>
  <div class="achivimentsCard Card">
    <div class="HeaderCard">
      <h3>Conquistas:</h3>
    </div>

     <!-- Achiviments -->
     <div class="scrollAchiviments">
      <!-- Achiviments Card -->
      <Achiviment/>
    </div>
  </div>
</template>

<script>
import Achiviment from './Achiviment.vue';
export default {
  name: "AchivimentsCard",
  components: {
    Achiviment
  }
}
</script>

<style>
  .scrollAchiviments {
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
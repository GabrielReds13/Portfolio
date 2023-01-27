<template>
  <div class="achiviment">
    <!-- Achivimet icon -->
    <div class="achivimentIcon">
      <div class="icon">
        <img src="@/assets/AchivimentIcons/HelloWorld.svg"> 
      </div>
    </div>

    <!-- Achiviment details -->
    <ul class="achivimentInfos">
      <li class="achivimentTitle">
        <p>Hello World!</p>
      </li>
      <li class="achivimentDescription">
        <p>De início a sua jornada.</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Achiviment"
}
</script>

<style scoped>
.achiviment {
  display: flex;
  flex-direction: row;

  width: 90%;
  height: 20%;
  min-height: 88px !important;
  
  align-items: center;

  border-left: 0.5vh solid #fff;
  border-radius: 0 1vh 1vh 0;

  background-color: #00000025;
  box-shadow: 0 0 4px 0 #00000025;

  margin-top: 5%;
  margin-bottom: 2%;
  margin-left: 1%;
}

/* Achiviment icon */
.achivimentIcon {
  display: flex;
  justify-content: center;
  align-items: center;

  min-width: 70px !important;
  width: 21%;
  min-height: 70px !important;
  height: 76%;

  margin-left: 3.5%;

  border-radius: 100%;
  background: linear-gradient(#FF002E, #7600BE);
}
.achivimentIcon .icon {
  display: flex;
  justify-content: center;
  align-items: center;

  width: 90%;
  height: 90%;

  border-radius: 100%;
  background: linear-gradient(#0D0D0D, #450014);
}
.achivimentIcon .icon img {
  width: 60%;
  height: 60%;
}

/* Achiviment description */
.achivimentInfos {
  display: flex;
  flex-direction: column;
  list-style: none;
  margin-left: 4%;
}
.achivimentTitle {
  font-weight: bold;
  font-size: 110%;
}
.achivimentDescription {
  font-size: 90%;
  color: #C4C4C4;
}
</style>
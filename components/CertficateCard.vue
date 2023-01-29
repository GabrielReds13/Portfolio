<template>
  <div class="certficateCard">
    <!-- Header card -->
    <div class="headerCard">
      <div class="titleCard">
        <img src="@/assets/icons/Stars.svg" alt="Estrelas">
        <h3>Certificados:</h3>
      </div>
    </div>

    
    <!-- Content card -->
    <div class="contentCard">
      <!-- Button left -->
      <div class="buttonLeft">
        <p>◀</p>
      </div>

      <!-- Certficates -->
      <div class="certficatesAll">
        <div v-for="certficateProps in showCertficates" :key="certficateProps.name">
          <Certficate :name="certficateProps.name" :origin="certficateProps.origin" :photo="certficateProps.photo" :workIcon="certficateProps.workIcon" :color="certficateProps.color" :backgroundColor="certficateProps.backgrounColor" />
        </div>
      </div>

      <!-- Button right -->
      <div class="buttonRight">
        <p>▶</p>
      </div>
    </div>
  </div>
</template>

<script>
import '@/styles/ButtonStyle.css';
import Certficate from "@/components/Certficate.vue"

export default {
  name: "CertficateCard",
  components: {
    Certficate,
  },
  data() {
    return {
      certficates: [
        {name: "Discover", origin: "Trilha Conectar", photo: "DiscoverConectar", workIcon: "RocketseatLogo", color: "#8257E5", backgrounColor: "linear-gradient(#0D0D0D, #1A0B3E)"},
      ],
      showCertficates: [{}],
      actualCertficates: [1, 2, 3]
    }
  },
  methods: {
    async setCertficates() {
      let getCertficates = []

      if (this.certficates.length >= 3) {
        getCertficates = [this.certficates[0], this.certficates[1], this.certficates[2]]
      } else if (this.certficates.length > 1 && this.certficates.length < 3) {
        getCertficates = [this.certficates[0], this.certficates[1]]
      } else {
        getCertficates = [this.certficates[0]]
      }
      
      this.showCertficates = getCertficates
    }
  },
  mounted() {
   this.setCertficates() 
  }
}
</script>

<style scoped>
  .certficateCard {
    display: flex;
    flex-direction: column;

    width: 92.5vw;
    height: 85vh;

    margin-top: 75vh;
    border-radius: 1vh;
    box-shadow: 0 0 4px 0 #00000025;

    background-color: #121212;
    color: #fff;
  }
  /* Header card */
  .headerCard {
  display: flex;
  flex-direction: row;
  
  width: 92.5%;
  height: 6vh;

  position: absolute;
  z-index: 2;

  border-radius: 1vh 1vh 0 0;
  align-items: center !important;

  background: linear-gradient(-45deg,#FF002E, #7600BE);
  color: #fff;
}
.titleCard {
  display: flex;
  flex-direction: row;
  transform: translateX(15%);
}
.titleCard img {
  margin-right: 5%;
}

/* Content card */
.contentCard {
  display: flex;
  flex-direction: row;

  width: 100%;
  height:82%;
  margin-top: 4%;

  justify-content: space-between;
  align-items: center;
}
.certficatesAll {
  display: flex;
  flex-direction: row;

  justify-content: space-evenly;

  width: 80%;
  height: 100%;
}
</style>
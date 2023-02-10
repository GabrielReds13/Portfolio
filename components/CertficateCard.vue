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
      <!-- Certficates -->
      <div v-for="certficateProps in certficates" :key="certficateProps.key">
        <Certficate :key="certficateProps.key" :nameWork="certficateProps.nameWork" :courseName="certficateProps.courseName" :certficate="certficateProps.certficate" />
      </div>
    </div>
  </div>
</template>

<script>
import Certficate from "@/components/Certficate.vue"

export default {
  name: "CertficateCard",
  components: {
    Certficate,
  },
  data() {
    return {
      certficates: [
        {key: 0 ,nameWork: "Rocketseat", courseName: "Discover - Conectar", certficate: "CertificadoConectar"},
      ],
    }
  },
  methods: {
  },
  mounted() {
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
  height:100%;
  margin-top: 4%;

  justify-content: initial;
  align-items: center;

  overflow-x: scroll;
  overflow-y: hidden;
}

/* Scrollbar */
::-webkit-scrollbar {
    height: 5px;
  }
  ::-webkit-scrollbar-thumb {
    background: #fff;
    border-radius: 90px;
  }
  ::-webkit-scrollbar-track {
    background: #1A1A1A;
  }

  /* Mobile */
  @media (max-width: 992px) { 
    .certficateCard {
      margin-top: 205vh;
    }
  }
</style>
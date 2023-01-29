<template>
  <div id="certficateCard" class="certficate">
    <!-- Work log -->
    <div id="workLogo" class="workLogo">
      <img  src="@/assets/workIcons/Rocketseat.svg" v-show="isRocketseat">
    </div>
    <!-- Content -->
    <div class="contentCertficateCard">
      <!-- Photo -->
      <img id="photoCertficate" src="@/assets/certficatePhoto/Rocketseat/Discover/Conectar.png" alt="Discover - Conectar" v-show="isDiscoverConectar">
      <!-- Details -->
      <h3 id="nameCertficate">{{ name }}</h3>
      <div class="dividerCertficate"></div>
      <p class="originCertficate">{{ origin }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Certficate",
  props: {
    name: String,
    origin: String,
    photo: String,
    workIcon: String,
    color: String,
    backgroundColor: String,
  },
  data() {
    return {
      isRocketseat: false,
      isDiscoverConectar: false
    }
  },
  methods: {
    async getStyleInCard() {
      document.getElementById("certficateCard").style.background = `${this.backgroundColor}`
      document.getElementById("certficateCard").style.border = `1vh solid ${this.color}`
      document.getElementById("workLogo").style.backgroundColor = `${this.color}`

      if(this.photo == "DiscoverConectar") {
        this.isDiscoverConectar = true
      } else {}
      
      if (this.workIcon == "RocketseatLogo") {
        this.isRocketseat = true
      } else {}
    }
  },
  mounted() {
    this.getStyleInCard()
  }
  
}
</script>

<style scoped>
  .workLogo {
    display: flex;
    flex-direction: column;
    position: absolute;
    z-index: 2;

    min-width: 50px !important;
    width: 8vh;
    min-height: 50px !important;
    height: 8vh;

    border-radius: 0 0 6vh 0;
  }
  .workLogo img {
    width: 50%;
    height: 50%;

    margin-top: 15%;
    margin-left: 15%;
  }
  /* Card */
  .certficate {
    width: 280px;
    height: 420px;

    margin-left: 1%;
    margin-right: 1%;

    border-radius: 1vh;
    border: 1vh solid #ffffff00;
    box-shadow: 0 0 4px 0 #00000025;
    cursor: pointer;

    background: #0D0D0D;

    color: #fff;
  }

  /* Content */
  .contentCertficateCard {
    display: flex;
    flex-direction: column;
    align-items: center;

    width: 100%;
    height: 100%;
  }
  .contentCertficateCard img {
    width: 250px;
    height: 250px;

    margin-top: 6%;
    border-radius: 4vh;
  }
  #nameCertficate {
    font-size: 150%;
    font-weight: bold;
    margin-top: 8%;
  }
  .dividerCertficate {
    width: 60%;
    height: 0.5vh;

    margin-top: 2%;
    margin-bottom: 2.5%;

    border-radius: 99px;
    background-color: #fff;
  }
</style>
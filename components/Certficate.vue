<template>
  <div :id='courseID.replace(" ", "")' class="certficate" @click="enableViewCertficate">
    <!-- Work log -->
    <div id="workLogo" class="workLogo">
      <img id="iconWorkLogo" src="@/assets/workIcons/Rocketseat.svg">
    </div>
    <!-- Content -->
    <div class="contentCertficateCard">
      <!-- Photo -->
      <img id="photoCertficate" src="@/assets/certficatePhoto/Rocketseat/Conectar/Conectar.png" :alt="courseName">
      <!-- Details -->
      <h3 id="nameCertficate">{{ nameWork }}</h3>
      <div class="dividerCertficate"></div>
      <p class="originCertficate">{{ courseName }}</p>
    </div>

    <viewCertficate :courseCertficate="courseCertficate" v-show="showCertficate" />
  </div>
</template>

<script>
import viewCertficate from "~~/components/viewCertficate.vue"

export default {
  name: "Certficate",
  components: {
      viewCertficate
  },
  props: {
    nameWork: String,
    courseName: String,
    certficate: String,
    key: Number
  },
  data() {
    return {
      courseID: `${this.nameWork}${this.key}`,
      courseCertficate: this.certficate,
      showCertficate: false
    }
  },
  methods: {
    enableViewCertficate() {
      if (this.showCertficate == false) {
        this.showCertficate = true
      } else {
        this.showCertficate = false
      }
    }
  },
}
</script>

<style scoped>
  .workLogo {
    display: flex;
    flex-direction: column;
    position: relative;

    min-width: 50px !important;
    width: 8vh;
    min-height: 50px !important;
    height: 8vh;

    border-radius: 0 0 6vh 0;
    background-color: #7600BE;
  }
  .workLogo img {
    width: 50%;
    height: 50%;

    margin-top: 15%;
    margin-left: 15%;
  }
  /* Card */
  .certficate {
    min-width: 280px !important;
    min-height: 450px !important;

    margin-left: 1vh;
    margin-right: 1vh;

    border-radius: 1vh;
    border: 1vh solid #7600BE;
    box-shadow: 0 0 4px 0 #00000025;
    cursor: pointer;

    background: linear-gradient(#0D0D0D, #540057);

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
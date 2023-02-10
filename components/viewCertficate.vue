<template>
  <div>
    <div id="viewCertificateScreen">
      <!-- Certificados -->
      <img src="@/assets/certficatePhoto/Rocketseat/Conectar/Certficado.png" :alt="courseCertficate" v-show="CertficateNumber == 0">
      
      <!-- Mensagem -->
      <p>Clique para fechar</p>
    </div>
  </div>
</template>

<script>
  export default {
    name: "viewCertficate",
    props: {
      courseCertficate: String
    },
    data() {
      return {
        CertficateNumber: 0
      }
    },
    methods: {
      async setCertficate() {
        if (this.courseCertficate == "CertificadoConectar") {
          this.CertficateNumber = 0
        }
      }
    },
    mounted() {
      this.setCertficate()
    }
  }
</script>

<style>
  #viewCertificateScreen {
    display: flex;
    flex-direction: column;

    width: 100vw;
    height: 100vh;

    justify-content: center;
    align-items: center;
    
    position: fixed;
    z-index: 5;
    left: 0;
    top: 0;

    background: linear-gradient(#0D0D0D50, #45001475);
    backdrop-filter: blur(2px);
  }
  #viewCertificateScreen img {
    width: 50%;
    box-shadow: 0 0 4px 0 #00000025;
    border-radius: 1vh;
  }
  #viewCertificateScreen p {
    position: fixed;
    bottom: 5vh;
  }
</style>
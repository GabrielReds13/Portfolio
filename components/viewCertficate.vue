<template>
  <div>
    <div id="viewCertificateScreen">

    </div>
  </div>
</template>

<script>
  export default {
    name: "viewCertficate"
  }
</script>

<style>
  #viewCertificateScreen {
    width: 100vw;
    height: 100vh;
    
    position: fixed;
    z-index: 5;
    left: 0;
    top: 0;

    background: linear-gradient(#0D0D0D50, #45001475);
    backdrop-filter: blur(2px);
  }
</style>
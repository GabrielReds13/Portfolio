<template>
  <div class="errorPage">
    <!-- Head page -->
    <head>
      <title>Erro 404...</title>
    </head>

    <!-- Content page -->
    <img src="@/assets/Illustrations/ErrorIlustration.svg" alt="Ilustração de erro">
    <div class="messageError">
      <p>Nenhum troféu foi encontrado.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "errorPage"
}
</script>

<style scoped>
  .errorPage {
    display: flex;
    flex-direction: column;

    width: 100vw;
    height: 100vh;

    justify-content: center;
    align-items: center;

    background: linear-gradient(#181818, #300017);
  }
  .messageError {
    display: flex;
    width: 25vw;
    height: 8vh;

    margin-top: 3%;

    border: 0.5vh solid #fff;
    color: #fff;
    border-radius: 999px;

    justify-content: center;
    align-items: center;
  }
</style>
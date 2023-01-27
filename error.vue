<template>
  <div class="errorPage">
    <!-- Head page -->
    <head>
      <title>Erro 404 jogador...</title>
    </head>

    <!-- Content page -->
    <img src="@/assets/Illustrations/ErrorIlustration.svg" alt="Ilustração de erro">
    <div class="messageError">
      <p>Nenhum troféu foi encontrado.</p>
    </div>

    <NuxtLink class="returnToHome" to="/">
        RETORNAR À HOME
    </NuxtLink>
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
    min-width: 275px !important;
    width: 25vw;
    height: 8vh;

    margin-top: 4vh;

    border: 0.5vh solid #fff;
    color: #fff;
    border-radius: 999px;

    justify-content: center;
    align-items: center;
  }
  .returnToHome {
    display: flex;

    min-width: 275px !important;
    width: 25vw !important;
    height: 8vh !important;

    justify-content: center;
    align-items: center;
    position: absolute;
    bottom: 5%;

    border-radius: 1vh;

    text-decoration: none;
    font-weight: bold;
    color: #fff;

    background-color: #FF002E;
    transition: 200ms ease-in-out;
  }
  .returnToHome:hover {
    background-color: #ff224a;
  }
</style>
<template>
  <div>
    <header class="header">
      <NuxtLink to="/"><p>Hello Everyone!</p></NuxtLink>
    </header>

    <div class="contentPage">
      <slot/>
    </div>
  </div>
</template>

<script>
export default {
  name: "default"
}
</script>

<style>
  body {
    overflow-x: hidden;
  }
  * {
    margin: 0;
    padding: 0;
  }
  .header {
    display: flex;
    flex-direction: row;

    position: absolute !important;
    z-index: 99 !important;

    width: 100vw;
    height: 50px;

    background-color: #181818;
    box-shadow: 0 0 4px 0 #00000025;
  }
  .contentPage {
    display: flex;
    width: 100vw;

    margin-top: 2vh;
    
    position: absolute !important;
    z-index: 1 !important;
  }
  
  /* Mobile */
  @media (max-width: 992px) { 
    .contentPage {
      margin-top: 6vh;
    }
  }
</style>
<template>
  <div class="userCard Card">
    <div class="userPhoto">
      <img :src="user.avatar_url" alt="Foto de perfil">
    </div>

    <h3 class="userName">{{ user.name }}</h3>
    <a :href="user.html_url" target="_blank" class="githubProfile">
      <img src="@/assets/GithubIcon.svg" alt="Logo do GitHub">
      <p class="userGithub">{{ user.login }}</p>
    </a>

    <div class="divider"></div>

    <p class="userBio">{{ user.bio }}</p>
  </div>
</template>

<script>
  import "@/styles/CardStyle.css"
  export default {
    name: "UserCard",
    data() {
      return {
        user: {
          isDev: true
        }
      }
    },
    methods: {
      getGithubProfileInfos() {
        const getUserData = fetch(`https://api.github.com/users/GabrielReds13`)
        .then(response => response.json())
        .then(data => this.user = data)
      }
    },
    mounted() {
      this.getGithubProfileInfos()
    }
  }
</script>

<style scoped>
  /* Foto do Usuario */
  .userPhoto {
    display: flex;

    min-width: 180px !important;
    width: 25vh;
    min-height: 180px !important;
    height: 25vh;

    justify-content: center;
    align-items: center;

    border-radius: 100%;
    margin-top: 10%;
    margin-bottom: 5%;

    background: linear-gradient(#FF002E, #7600BE);
  }
  .userPhoto img {
    width: 85%;
    height: 85%;

    border: 1.3vh solid #121212; 

    border-radius: 100%;
  }

  /* Divider */
  .divider {
    width: 60%;
    height: 0.5%;

    margin: 6%;
    border-radius: 999px;

    background-color: #fff;
  }
  /* Texto */
  .userName {
    font-size: 24px;
  }
  .githubProfile {
    display: flex;
    flex-direction: row;

    width: 36%;

    justify-content: space-between;
    text-decoration: none;
    color: #C4C4C4;
  }
  .userBio {
    text-align: center;
    color: #C4C4C4;
    width: 75%;
  }
  
</style>
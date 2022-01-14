<template>
  <v-container class="pt-15 mt-10 mb-10">
    <v-row class="responsiveness">
      <v-col lg="6">
        <h2 class="intro-text"><v-icon class="icon">mdi-fingerprint</v-icon> DigitalWeb</h2>
        <h3 class="intro-subtext">Transforme a sua ideia em realidade!</h3>
        <p class="description">
          Projetamos, desenvolvemos e gerenciamos produtos digitais de alto impacto que geram leads, vendem e contam
          histórias.
        </p>
        <v-btn color="success" rounded elevation="2" class="white--text mr-5 my-1">Faça um Orçamento</v-btn>
        <v-btn outlined rounded>
          <v-icon style="margin-right: 10px" class="my-1">mdi-play-circle</v-icon> Saiba Mais
        </v-btn>
      </v-col>
      <v-col lg="6">
        <img width="100%" src="../assets/team_logo.svg" alt="" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HeroComponent",
};
</script>

<style scoped>
.intro-text {
  font-size: 70px;
  font-weight: 800;
  transition: 0.4s ease all;
  cursor: default;
}
.intro-text:hover {
  letter-spacing: 2px;
}
.intro-subtext {
  margin-top: 1rem;
  font-size: 30px;
}
.icon {
  font-size: 70px;
}
@media (max-width: 968px) {
  .responsiveness {
    display: flex;
    flex-direction: column-reverse;
  }
  .intro-text {
    font-size: 55px;
    display: flex;
    flex-direction: row-reverse;
  }
  .intro-subtext {
    margin-top: 10px;
    font-size: 30px;
  }
}
</style>

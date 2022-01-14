<template>
  <div class="container">
    <v-row justify="center" class="responsiveness">
      <v-col lg="12" class="text-center">
        <v-subheader class="text-h4 justify-center">Entre em Contato</v-subheader>
        <p>
          Estamos ansiosos para descobrir como podemos trabalhar juntos e transformar os seus sonhos em realidade. Mande
          uma mensagem pra gente!
        </p>
      </v-col>
      <v-col lg="6"
        ><iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d56438.3224327658!2d-46.65091451608411!3d-23.566070269536723!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94ce448183a461d1%3A0x9ba94b08ff335bae!2zU8OjbyBQYXVsbywgU1A!5e0!3m2!1spt-BR!2sbr!4v1642177683049!5m2!1spt-BR!2sbr"
          width="100%"
          height="100%"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
        ></iframe
      ></v-col>
      <v-col lg="6">
        <v-form ref="form" v-model="valid" lazy-validation>
          <v-text-field v-model="contactInfo.name" :counter="15" label="Nome" required></v-text-field>

          <v-text-field v-model="contactInfo.email" label="E-mail" required></v-text-field>

          <v-textarea label="Mensagem" v-model="contactInfo.message" no-resize></v-textarea>

          <v-btn color="success" class="mr-4" @click="validate"> Enviar </v-btn>
        </v-form>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "ContactUs",
  data: () => ({
    contactInfo: {},
  }),
};
</script>

<style scoped>
.container {
  margin-bottom: 3rem;
}
@media (max-width: 968px) {
  .responsiveness {
    display: flex;
    flex-direction: column;
  }
}
</style>

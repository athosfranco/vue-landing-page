<template>
  <v-app>
    <Header />
    <v-main>
      <HeroComponent />
      <AboutUs />
      <Projects />
      <Gallery />
      <ContactUs />
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
import Header from "./components/Header.vue";
import HeroComponent from "./components/HeroComponent.vue";
import AboutUs from "./components/AboutUs.vue";
import Projects from "./components/Projects.vue";
import Gallery from "./components/Gallery.vue";
import Footer from "./components/Footer.vue";
import ContactUs from "./components/ContactUs.vue";

export default {
  name: "App",
  components: { Header, HeroComponent, AboutUs, Projects, Gallery, Footer, ContactUs },
};
</script>

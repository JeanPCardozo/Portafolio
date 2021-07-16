<template>
  <div>
    <Header :msg="header" />
    <Container />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Container from "./components/Container.vue";
export default {
  name: "App",
  data: () => ({
    header: "Portafolio GH",
  }),
  components: {
    Header,
    Footer,
    Container,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");

* {
  margin: 0px;
  padding: 0px;
  font-family: "Roboto", sans-serif;
}
</style>

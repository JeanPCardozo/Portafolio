<template>
  <div id="container" class="container">
    <h2>Proyectos</h2>
    <hr />
    <div id="cards">
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";
export default {
  components: {
    Card,
  },
};
</script>

<style>
#cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.container {
  overflow: hidden;
  text-align: center;
  padding: 7px;
  margin: 1rem;
  border: solid 1px #eee;
  box-shadow: 1px 1px 4px #333;
}
</style>

<template>
  <div>
    <header>
      <h2>{{ msg }}</h2>
    </header>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    msg: String,
  },
};
</script>

<style scoped>
header {
  text-align: center;
  background-color: rgb(51, 51, 51);
  padding: 1rem;
  color: #eee;
  margin: 0px;
}
</style>

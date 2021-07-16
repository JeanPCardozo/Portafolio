<template>
  <div>
    <footer>
      <h2>&copy; {{ year }} {{ author }}</h2>
    </footer>
  </div>
</template>

<script>
export default {
  name: "Header",
  data: () => ({
    author: "Jean Cardozo",
  }),
  computed: {
    year() {
      return new Date().getFullYear();
    },
  },
};
</script>

<style scoped>
footer {
  text-align: center;
  background-color: rgb(51, 51, 51);
  padding: 1rem;
  color: #eee;
  margin: 0px;
}
</style>

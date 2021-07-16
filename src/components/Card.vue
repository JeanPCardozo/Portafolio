<template>
  <div id="card" class="card">
    <h4>{{ name }}</h4>

    <a :href="htmlUrl">{{ htmlUrl }}</a>

    <p>
      {{ description }}
    </p>
    <p>
      <strong>{{ author }}</strong>
    </p>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    htmlUrl: String,
    description: String,
    author: String,
  },
};
</script>

<style scoped>
.card {
  word-wrap: break-word;
  width: 250px;
  margin: 7px;
  text-align: center;
  border: solid 1px #eee;
  box-shadow: 1px 1px 4px #333;
}
</style>

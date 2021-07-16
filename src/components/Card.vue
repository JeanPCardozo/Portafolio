<template>
  <div id="card" class="card">
    <h4>{{ name }}</h4>
    <p>
      {{ description }}
    </p>
    <p>
      <strong>{{ author }}</strong>
    </p>
    <br />
    <div class="d-flex justify-content-around">
      <button type="button" class=" btn btn-info">
        <a :href="htmlUrl" target="_blank">Github</a>
      </button>
      <button v-if="homepage != null" type="button" class=" btn btn-success">
        <a :href="homepage" target="_blank">Web</a>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    htmlUrl: String,
    description: String,
    author: String,
    homepage: String,
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

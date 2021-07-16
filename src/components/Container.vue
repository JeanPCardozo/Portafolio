<template>
  <div id="container" class="container">
    <h2>Proyectos</h2>
    <img
      class="avatar"
      :src="avatar"
      alt="Avatar de JeanPCardozo"
      loading="lazy"
    />
    <hr />
    <div id="cards">
      <Card
        v-for="project in projects"
        :key="project.id"
        :name="project.name"
        :htmlUrl="project.html_url"
        :description="project.description"
        :author="project.owner.login"
      />
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";
export default {
  data: () => ({
    projects: null,
    avatar: null,
  }),
  components: {
    Card,
  },
  methods: {
    async getProyects() {
      const res = await fetch(
        "https://api.github.com/users/JeanPCardozo/repos"
      );
      const data = await res.json();
      this.projects = data;
      this.avatar = this.projects[0].owner.avatar_url;
      console.log(this.projects);
    },
  },
  mounted() {
    this.getProyects();
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

.avatar {
  width: 100px;
  height: 100px;
  border-radius: 50px;
}
</style>

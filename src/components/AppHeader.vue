<template>
  <header>
    <!-- <nav>
      <router-link to="/">Vue Trello</router-link> |
      <router-link to="/about">About</router-link>
    </nav> -->
    <span class="title">Vue Trello</span>
    <router-link class="btn-header" to="/">Mis paneles </router-link>
  </header>
</template>

<script>
export default {
  name: 'app-header',
};
</script>

<style scoped>
header {
  box-sizing: border-box;
  background-color: black;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  margin: 0;
  padding: 1rem;
}
.title {
  align-self: center;
  color: #eceff1;
  font-size: 2rem;
  font-weight: bold;
  margin-right: 1rem;
}
.btn-header {
  background-color: #97b924;
  border: none;
  border-radius: 10px;
  box-shadow: 0 0 0 0.5px rgba(49, 49, 93, 0.03),
    0 2px 5px 0 rgba(49, 49, 93, 0.03), 0 1px 2px 0 rgba(0, 0, 0, 0.08);
  color: #203483;
  cursor: pointer;
  font-size: 2rem;
  text-decoration: none;
  padding: 0.5rem;
  margin: 0 0.5rem;
}
</style>

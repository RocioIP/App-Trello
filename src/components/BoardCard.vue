<template>
  <router-link class="board-card" to="{ name: 'board', params: { name, id } }">
    <span class="board-card-title"> {{ name }}</span>
  </router-link>
</template>

<script>
export default {
  name: 'board-card',
  props: {
    id: String,
    name: String,
  },
};
</script>

<style scoped>
.board-card {
  background-color: #97b924;
  box-shadow: 0 0 0 0.5px rgba(49, 49, 93, 0.03),
    0 2px 5px 0 rgba(49, 49, 93, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.08);
  box-sizing: border-box;
  border-radius: 5px;
  color: #203483;
  margin: 0.5rem 1.5rem;
  padding: 1rem;
  text-align: left;
  text-decoration: none;
  transition: all 600ms ease;
  width: 200px;
}
.board-card-title {
  font-size: 1.2rem;
}
.board-card:hover {
  background-color: #aac25a;
  font-weight: bold;
}
@media screen and (min-width: 600px) {
  .board-card {
    width: 25%;
  }
}
@media screen and (min-width: 1024px) {
  .board-card {
    width: 150px;
  }
}
</style>

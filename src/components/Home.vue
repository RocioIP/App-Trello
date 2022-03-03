<template>
  <div>
    <h2>Mis Paneles</h2>
    <div class="boards-collection">
      <input
        type="text"
        placeholder="Añade un nuevo panel"
        v-model="boardName"
        @keyup.enter="add()"
      />
      <board-card
        v-for="(board, index) in boards"
        :key="index"
        :name="board.name"
        :id="board.id"
      >
      </board-card>
    </div>
  </div>
</template>

<script>
import BoardCard from '@/components/BoardCard';
export default {
  name: 'HelloWorld',
  components: { BoardCard },
  data: function () {
    return {
      boardName: '',
      boards: [
        { id: 1, name: 'Tareas' },
        { id: 2, name: 'Lista de la compra' },
      ],
    };
  },
  methods: {
    add: function () {
      this.boards.push({ name: this.boardName });
    },
  },
};
</script>

<style scoped>
h2 {
  text-align: center;
  margin: 1.5rem;
  color: #203483;
}
.boards-collection {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  padding-top: 1rem;
}
input {
  box-sizing: border-box;
  background-color: #cfd8dc;
  border: 2px solid #808e92;
  border-radius: 3px;
  font-size: 1.1rem;
  outline: 0;
  padding: 0.5rem;
  transition: all 600ms ease;
}
input:focus,
:active {
  background-color: white;
  color: #203483;
}
input::placeholder {
  color: #1c1f20;
}
</style>

<template>
  <div class="container">
    <h1>Atividades do dia</h1>

    <ul>
      <li v-for="item in tarefas" :key="item.id">
        <p v-if="item.estaCompleta" class="completo">{{ item.descricao }}</p>
        <p v-else class="incompleto">{{ item.descricao }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "daylist",
  data() {
    return {
      tarefas: [
        { id: 0, descricao: "Fazer dever", estaCompleta: true },
        { id: 1, descricao: "Andar", estaCompleta: true },
        { id: 2, descricao: "Passear com o chachorro", estaCompleta: false },
        { id: 3, descricao: "Assistir a aula", estaCompleta: true },
        { id: 4, descricao: "Estudar Vue", estaCompleta: false },
        { id: 5, descricao: "Assistir filme", estaCompleta: false },
      ],
    };
  },
};
</script>

<style scoped>
h1 {
  background: white;
  text-align: center;
}

.container {
  background: white;
  width: 920px;

  padding: 10px;
  border-radius: 5px;
  margin: 50px auto;
}

.container ul {
  background: white;
  list-style: flex;
  margin: 0 auto;
}

.incompleto {
  color: red;
  background: white;
}

.completo {
  color: green;
  background: white;
}
</style>

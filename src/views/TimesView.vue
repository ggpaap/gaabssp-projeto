<script>
export default {
  data() {
    return {
      times: [
        { id: 1, nome: "Time 1" },
        { id: 2, nome: "TIme 2" },
        { id: 3, nome: "Time 3" },
      ],
    };
  },
};
</script>

<template>
  <div class="container">
    <div class="title">
      <h2>Gerenciamento de Times</h2>
    </div>
    <div class="form-input">
      <input type="text" />
      <button>Salvar</button>
    </div>
    <div class="list-times">
      <table>
        <thead>
          <tr>
            <th>ID</th>
            <th>Nome</th>
            <th>Ações</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="time in times" :key="time.id">
            <td>{{ time.id }}</td>
            <td>{{ time.nome }}</td>
            <td>_________</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
  <RouterView />
</template>

<style>
.title {
  text-align: center;
  margin: 2rem 0;
}

.form-input {
  display: flex;
  justify-content: center;
  margin: 2rem 0;
}

.form-input input {
  width: 50%;
  padding: 0.5rem;
  border: 5px solid #98b7e1;
  border-radius: 10px;
}

.form-input button {
  padding: 0.5rem;
  border: 5px solid #98b7e1;
  border-radius: 10px;
  color: #454663;
  font-weight: bold;
  margin-left: 1%;
}

.list-times {
  display: flex;
  justify-content: center;
}

table {
  width: 80%;
  border-collapse: collapse;
  margin: 0 auto;
  border: 1px solid #9bfae2;
  font-size: 1.1rem;
  text-align: center;
}

table thead {
  background-color: #18283d;
  color: #d4d4d4;
}

table thead th {
  font-weight: bolder;
}

table tbody tr:nth-child(odd) {
  background-color: #81848d;
}
</style>

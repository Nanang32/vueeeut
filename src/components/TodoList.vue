<template>
  <div class="container">
    <h2>Todo List Vue JS</h2>

    <input v-model="task" placeholder="Masukkan tugas" />
    <button @click="addTask">Tambah</button>

    <ul>
      <li v-for="(item,index) in tasks" :key="index">
        {{ item }}
        <button @click="removeTask(index)">Hapus</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      task: '',
      tasks: []
    }
  },

  methods: {
    addTask() {
      if (this.task !== '') {
        this.tasks.push(this.task)
        this.task = ''
      }
    },

    removeTask(index) {
      this.tasks.splice(index, 1)
    }
  }
}
</script>

<style>
body{
  font-family: Arial;
  background: #f2f2f2;
}

.container{
  width: 400px;
  margin: auto;
  background: white;
  padding: 20px;
  border-radius: 10px;
  margin-top: 50px;
}

input{
  width: 70%;
  padding: 10px;
}

button{
  padding: 10px;
  margin-left: 5px;
}

li{
  margin-top: 10px;
}
</style>
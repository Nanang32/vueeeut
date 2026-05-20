<template>
  <div class="container">

    <h1>Contoh Data Binding Vue JS</h1>

    <input v-model="nama" placeholder="Masukkan nama">

    <br><br>

    <input v-model="umur" type="number" placeholder="Masukkan umur">

    <br><br>

    <select v-model="jurusan">
      <option>Sistem Informasi</option>
      <option>Informatika</option>
      <option>Teknik Komputer</option>
    </select>

    <hr>

    <h2>Hasil Data Binding</h2>

    <p>Nama : {{ nama }}</p>
    <p>Umur : {{ umur }}</p>
    <p>Jurusan : {{ jurusan }}</p>

  </div>
</template>

<script>
export default {
  data() {
    return {
      nama: '',
      umur: '',
      jurusan: 'Sistem Informasi'
    }
  }
}
</script>

<style>
.container{
  width: 400px;
  margin: auto;
  padding: 20px;
  font-family: Arial;
}

input, select{
  width: 100%;
  padding: 10px;
}
</style>
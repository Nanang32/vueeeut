<template>
  <div class="container">

    <h1>Data Mahasiswa</h1>

    <!-- Input -->
    <input 
      v-model="keyword"
      placeholder="Cari nama mahasiswa"
    >

    <br><br>

    <!-- Event Handling -->
    <button @click="tambahData">
      Tambah Data
    </button>

    <hr>

    <!-- Array + Filter -->
    <ul>
      <li v-for="(mhs,index) in filterMahasiswa" :key="index">

        {{ mhs }}

        <button @click="hapusData(index)">
          Hapus
        </button>

      </li>
    </ul>

  </div>
</template>

<script>
export default {

  data() {
    return {
      keyword: '',

      mahasiswa: [
        'Andi',
        'Budi',
        'Luqman',
        'Sinta'
      ]
    }
  },

  computed: {

    // FILTER
    filterMahasiswa() {

      return this.mahasiswa.filter((item) => {

        return item
          .toLowerCase()
          .includes(this.keyword.toLowerCase())

      })

    }

  },

  methods: {

    // EVENT HANDLING
    tambahData() {

      this.mahasiswa.push('Mahasiswa Baru')

    },

    hapusData(index) {

      this.mahasiswa.splice(index,1)

    }

  }

}
</script>

<style>
.container{
  width: 400px;
  margin: auto;
  font-family: Arial;
}

input{
  width: 100%;
  padding: 10px;
}

button{
  margin-left: 5px;
  padding: 5px 10px;
}

li{
  margin-top: 10px;
}
</style>
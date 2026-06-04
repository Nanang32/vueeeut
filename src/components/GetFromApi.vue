<template>
  <div>

    <h2>Data Pengguna</h2>

    <table border="1" cellpadding="10">
      <thead>
        <tr>
          <th>ID</th>
          <th>Nama</th>
          <th>Email</th>
          <th>Kota</th>
          <th>Jalan</th>
          <th>nomor rumah</th>
          <th>titik kordinat</th>
          <th>Kode Pos</th>
          <th>Telepon</th>
          <th>Perusahaan</th>
        </tr>
      </thead>

      <tbody>
        <tr v-for="user in users" :key="user.id">
          <td>{{ user.id }}</td>
          <td>{{ user.name }}</td>
          <td>{{ user.email }}</td>
          <td>{{ user.address.city }}</td>
          <td>{{ user.address.street }}</td>
          <td>{{ user.address.suite }}</td>
          <td>{{ user.address.geo.lat }}, {{ user.address.geo.lng }}</td>
          <td>{{ user.address.zipcode }}</td>
          <td>{{ user.phone }}</td>
          <td>{{ user.company.name }}</td>
        </tr>
      </tbody>

    </table>

  </div>
</template>

<script>
import axios from 'axios'

export default {

  data() {
    return {
      users: []
    }
  },

  mounted() {

    axios
      .get('https://jsonplaceholder.typicode.com/users')
      .then(response => {
        this.users = response.data
      })
      .catch(error => {
        console.log(error)
      })

  }

}
</script>

<style>
table{
  width: 100%;
  border-collapse: collapse;
}

th{
  background-color: #42b883;
  color: white;
}

th, td{
  padding: 10px;
  text-align: left;
}
</style>
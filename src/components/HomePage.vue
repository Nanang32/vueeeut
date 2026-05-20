<template>
  <div class="content">

    <h1>Selamat Datang</h1>

    <p>
      Ini adalah contoh halaman sederhana Vue JS.
    </p>

    <button @click="klikSaya">
      Klik Saya
    </button>

  </div>
</template>

<script>
export default {

  methods: {

    klikSaya() {
      alert('Tombol berhasil diklik')
    }

  }

}
</script>

<style>
.content{
  padding: 30px;
  font-family: Arial;
}

button{
  padding: 10px 20px;
  cursor: pointer;
}
</style>
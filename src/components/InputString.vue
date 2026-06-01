<template>
  <div>
    <input v-model="nama" placeholder="Masukkan nama">

    <h2>Halo, {{ nama }}</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nama: ''
    }
  }
}
</script>
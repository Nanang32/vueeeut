<template>
  <div>
    <h1>{{ nama }}</h1>
    <p>Umur saya {{ umur }} tahun</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nama: 'Luqman',
      umur: 20
    }
  }
}
</script>
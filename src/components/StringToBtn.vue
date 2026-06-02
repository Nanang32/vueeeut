<template>
  <div>
    <h2>{{ status }}</h2>

    <button @click="ubahStatus">Ubah Status</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      status: "Belum Login",
    };
  },

  methods: {
    ubahStatus() {
      this.status = "Sudah Login";
    },
  },
};
</script>

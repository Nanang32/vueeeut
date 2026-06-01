<template>
  <div>
    <h2>Canvas Sederhana</h2>

    <canvas
      ref="canvas"
      width="300"
      height="150"
      style="border:1px solid black"
    >
    </canvas>
  </div>
</template>

<script>
export default {

  mounted() {

    const canvas = this.$refs.canvas
    const ctx = canvas.getContext('2d')

    let x = 10

    setInterval(() => {

      ctx.clearRect(0, 0, 300, 150)

      ctx.fillRect(x, 50, 50, 50)

      x += 5

      if (x > 300) {
        x = 0
      }

    }, 100)

  }

}
</script>
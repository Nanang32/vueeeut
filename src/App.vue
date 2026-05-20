<!-- <template>
  <ArrayAllData />
</template>

<script>
import ArrayAllData from './components/ArrayAllData.vue'

export default {
  components: {
    ArrayAllData
  }
}
</script> -->


<!-- <template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style> -->


<template>

  <div>

    <HeaderNav />

    <HomePage />

  </div>

</template>

<script>

import HeaderNav from './components/HeaderNav.vue'
import HomePage from './components/HomePage.vue'

export default {

  components: {
    HeaderNav,
    HomePage
  }

}

</script>
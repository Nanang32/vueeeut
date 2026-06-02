<!-- <template>
  <ArrayAllData />
</template>

<script>
import ArrayAllData from './components/ArrayAllData.vue'

export default {
  components: {
      
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
    <!-- HEADER -->
    <HeaderNav @gantiHalaman="halaman = $event" />
    <!-- HALAMAN -->
    <HomePage v-if="halaman == 'home'" />
    <AboutPage v-if="halaman == 'about'" />
    <ContactPage v-if="halaman == 'contact'" />
    <TodoList v-if="halaman == 'TodoList'" />
    <ArrayAllData v-if="halaman == 'ArrayAllData'" />
    <DataBinding v-if="halaman == 'DataBinding'" />
    <Animation v-if="halaman == 'Animation'" />
    <GetFromApi v-if="halaman == 'GetFromApi'" />
    <ExpString v-if="halaman == 'ExpString'" />
    <StringBinding v-if="halaman == 'StringBinding'" />
    <InputString v-if="halaman == 'InputString'" />
    <StringToBtn v-if="halaman == 'StringToBtn'" />
  </div>
</template>

<script>
import HeaderNav from "./components/HeaderNav.vue";
import HomePage from "./components/HomePage.vue";
import ContactPage from "./components/ContactPage.vue";
import AboutPage from "./components/AboutPage.vue";
import TodoList from "./components/TodoList.vue";
import ArrayAllData from "./components/ArrayAllData.vue";
import DataBinding from "./components/DataBinding.vue";
import Animation from "./components/ExpAnimation.vue";
import GetFromApi from "./components/GetFromApi.vue";
import ExpString from "./components/ExpString.vue";
import StringBinding from "./components/StringBinding.vue";
import InputString from "./components/InputString.vue";
import StringToBtn from "./components/StringToBtn.vue";

export default {
  components: {
    HeaderNav,
    HomePage,
    ContactPage,
    AboutPage,
    TodoList,
    ArrayAllData,
    DataBinding,
    Animation,
    GetFromApi,
    ExpString,
    StringBinding,
    InputString,
    StringToBtn,
  },

  data() {
    return {
      halaman: "home",
    };
  },
};
</script>
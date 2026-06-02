<template>
  <nav class="navbar">
    <h2>My Vue App</h2>

    <ul>
      <li>
        <a href="#" @click.prevent="$emit('gantiHalaman', 'home')"> Home </a>
      </li>

      <li>
        <a href="#" @click.prevent="$emit('gantiHalaman', 'about')"> About </a>
      </li>

      <li>
        <a href="#" @click.prevent="$emit('gantiHalaman', 'contact')">
          Contact
        </a>
      </li>

      <li>
        <a href="#" @click.prevent="$emit('gantiHalaman', 'TodoList')">
          Todo List
        </a>
      </li>

      <li>
        <a href="#" @click.prevent="$emit('gantiHalaman', 'ArrayAllData')">
          Array All Data
        </a>
      </li>

      <li>
        <a href="#" @click.prevent="$emit('gantiHalaman', 'DataBinding')">
          Data Binding
        </a>
      </li>

      <li>
        <a href="#" @click.prevent="showMenu = !showMenu">
          String Expression ▼
        </a>

        <ul v-if="showMenu" class="submenu">
          <li>
            <a href="#" @click.prevent="$emit('gantiHalaman', 'ExpString')">
              Exp
            </a>
          </li>
          <li>
            <a href="#" @click.prevent="$emit('gantiHalaman', 'InputString')">
              Input Expression
            </a>
          </li>
          <li>
            <a href="#" @click.prevent="$emit('gantiHalaman', 'StringToBtn')">
              Button
            </a>
          </li>
          <li>
            <a href="#" @click.prevent="$emit('gantiHalaman', 'StringBinding')">
              Binding
            </a>
          </li>
        </ul>
      </li>

      <li>
        <a href="#" @click.prevent="$emit('gantiHalaman', 'Animation')">
          Animation
        </a>
      </li>
      <li>
        <a href="#" @click.prevent="$emit('gantiHalaman', 'GetFromApi')">
          Get From Api
        </a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      showMenu: false,
    };
  },
};
</script>

<style>
.navbar {
  background: #42b883;
  color: white;
  padding: 15px;

  display: flex;
  justify-content: space-between;
  align-items: center;
}

ul {
  display: flex;
  gap: 20px;
  list-style: none;
}

a {
  color: white;
  text-decoration: none;
}
</style>

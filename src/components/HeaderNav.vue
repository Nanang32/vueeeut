<template>
  <nav class="navbar">

    <h2>My Vue App</h2>

    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Contact</a></li>
    </ul>

  </nav>
</template>

<style>
.navbar{
  background: #42b883;
  color: white;
  padding: 15px;

  display: flex;
  justify-content: space-between;
  align-items: center;
}

ul{
  display: flex;
  gap: 20px;
  list-style: none;
}

a{
  color: white;
  text-decoration: none;
}
</style>
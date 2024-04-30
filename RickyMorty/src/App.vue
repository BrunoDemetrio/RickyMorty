<script setup>
import {ref} from 'vue'
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark border-bottom border-body">
    <div class="container-fluid">
      
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="dropdown">
        <button class="btn btn-secondary dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
        RickyMorty
        </button>
        <ul class="dropdown-menu">
          <router-link class="dropdown-item" to="/">Home</router-link><br>
          <router-link class="dropdown-item" to="/about">About</router-link>
        </ul>
      </div>
    </div>
  </nav>

  <div class="main">
    <router-view></router-view>
  </div>

  <footer class="bg-dark text-light">
    <div>
      Unimar | ADS | {{ new Date().getFullYear() }}
    </div>
  </footer>
</template>
<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');
footer{
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 40px;
}
body{
  background-color: ghostwhite[];
  font-family: Roboto, sans-serif;
  font-style: normal;
}
</style>
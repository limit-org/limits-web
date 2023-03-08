<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import Header from './components/Header.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <Header/>
    </div>
  </header>
</template>

<style scoped>
header{
  display:grid;
  background-color:#2b2b57;
  height:10%;
  filter: drop-shadow(-2px 1px 7px #000);
  color:#EEEEEE;
}
</style>

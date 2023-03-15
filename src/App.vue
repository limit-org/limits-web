<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import Header from './components/Header.vue'
import TopicBar from './components/Topicbar.vue'
import $ from 'jquery'
import { ref } from 'vue'

function tbshow(){
  const element = document.getElementById("topicbar");
  element!.style.display = 'none';
}

</script>


<template>
  <header>
      <Header/>
  </header>
  <div id="topicbar" @show="tbshow">
    <TopicBar/>
  </div>
</template>

<style scoped>
header{
  height:8%;
  display:grid;
  grid-template-rows:60% 40%;
  grid-template-columns:16% 20% 30% 14% 20%;
  justify-content:center;
  place-items:center;
  grid-template-areas:
  "a0 b0 c0 d0 e0"
  "a1 b1 c1 d1 e1";
  background-color:#41306E;
  filter: drop-shadow(-2px 1px 7px #000);
  color:#EEEEEE;
}
#topicbar{
  height:5%;
  background-color:#5F3485;
  display:grid;
  justify-content:center;
  place-items:center;
  grid-template-rows:15% 70% 15%;
  grid-template-columns: 20% 20% 20% 20% 20%;
  grid-template-areas:
  "a0 b0 c0 d0 e0"
  "a1 b1 c1 d1 e1"
  "a2 b2 c2 d2 e2";
  color:#EEEEEE;
}
.hide{
  display:none;
}
</style>


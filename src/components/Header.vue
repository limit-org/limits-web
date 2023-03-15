<script setup lang="ts">
import $ from 'jquery';
function flip(){
    const $arrow = $("#header_arrow");
    const isFlipped = $arrow.hasClass("flipp");

    if(isFlipped) {
        $arrow.removeClass("flipp");
        $arrow.css({"transform":"rotate(0deg)", "transition-duration":"1s"});
    } else{
        $arrow.addClass("flipp");
        $arrow.css({"transform":"rotate(180deg)", "transition-duration":"1s"});
    }}
</script>

<template>
    <h1 id="header_icon">Limits</h1>
    <input type="text" id="header_search" placeholder="Search posts and communities..."/>
    <div id="header_contact">Contact</div>
    <div id="header_topics" @click="flip(); $emit('show')">Topics<img id="header_arrow" class="arrow flipp" src="./assets/down.svg" alt="down"></div>
    <div id="header_about">About Us</div>
    <div id="header_login">Login</div>
    <div id="header_signup">Sign Up</div>
    <hr>
</template>

<style scoped>
#header_icon{
    height:10%;
}
#header_search{
    width:90%;
    grid-area:c0;
}
#header_contact{
    grid-area:c1;
    margin-right:60%;
    margin-bottom:2%;
    font-weight:900;
    padding:2%;
}
#header_topics{
    grid-area:c1;
    margin-bottom:2%;
    font-weight:900;
    margin-right:5%;
}
#header_arrow{
    margin-left:8px;
}
#header_about{
    margin-left:50%;
    margin-bottom:2%;
    grid-area:c1;
    font-weight:900;
    padding:2%;
}
#header_login{
    padding-bottom:2%;
    padding-top:2%;
    padding-left:5%;
    padding-right:5%;
    grid-area:e0;
    font-weight:900;
    border:1px solid white;
}
@keyframes signupgrad{
    0% {background-position:0% 50%;}
    50% {background-position:100% 50%;}
    100% {background-position:0% 50%;}
}
#header_signup{
    background: linear-gradient(45deg, #5F3485, #BC96E6);
    padding:3%;
    padding-top:1.5%;
    margin-bottom:6%;
    grid-area:e1;
    font-weight:900;
    border:1px solid white;
    margin-top:5%;
    background-size: 400% 400%;
    animation: signupgrad 10s ease infinite;
}
</style>

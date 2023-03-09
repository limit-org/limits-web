<script setup lang="ts">
</script>

<template>
    <h1 id="header_icon">Limits</h1>
    <input type="text" id="header_search" placeholder="Search posts and communities..."/>
    <div id="header_contact">Contact</div>
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
}
#header_about{
    margin-left:50%;
    margin-bottom:2%;
    grid-area:c1;
    font-weight:900;
}
#header_login{
    background:#5F3485;
    padding-bottom:2%;
    padding-top:2%;
    padding-left:5%;
    padding-right:5%;
    grid-area:e0;
    font-weight:900;
}
#header_signup{
    background:#5F3485;
    padding:3%;
    padding-top:1.5%;
    margin-bottom:6%;
    grid-area:e1;
    font-weight:900;
    border-top:2px solid #41306E;
}
</style>

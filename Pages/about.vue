<template>
    <div>
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="/about">About</NuxtLink>
        Hello about
        <button @click="takeMetoPage">Take me to Home</button>
    </div>
</template>
<script setup>
function takeMetoPage(){
    navigateTo('/')
} 
</script>
<template>
    <div>
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="/about">About</NuxtLink>
        Hello index
        <button @click="takeMetoPage">Take me to About</button>
    </div>
</template>
<script setup>
function takeMetoPage(){
    navigateTo('about')
} 
</script>
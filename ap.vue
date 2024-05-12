<!-- Dynamic Components -->
<!-- <template>
  <button @click="toggle">Toggle</button>
  <component :is="Mycomponent"></component>
</template>

<script setup>
const Mycomponent = shallowRef(resolveComponent("Counter"));

function toggle() {
  if (Mycomponent.value === resolveComponent("Counter")) {
    Mycomponent.value = resolveComponent("HomeWelcome");
  } else {
    Mycomponent.value = resolveComponent("Counter");
  }
}
</script> -->

<!-- Dynamic Imports -->
<template>
  <a href="#" @click="view('home')">Home</a>
  <a href="#" @click="view('counter')">Counter</a>
  <NuxtPage/>
  <LazyHomeWelcome v-if="page=='home'"/>
  <LazyCounter v-if="page=='counter'"/>
</template>

<script setup>
const page = ref('home');
function view(name){
  page.value=name;
}
</script>

<!-- // Asynchronous function that returns a promise
function asyncOperation() {
    return new Promise((resolve, reject) => {
        // Simulate asynchronous operation
        setTimeout(() => {
            const randomNumber = Math.random();
            if (randomNumber > 0.5) {
                resolve(randomNumber); // Resolve the promise with a random number
            } else {
                reject(new Error("Random number is less than or equal to 0.5")); // Reject the promise with an error
            }
        }, 3000); // Simulate 1 second delay
    });
}

// Using the async operation with then and catch
asyncOperation()
    .then(result => {
        setTimeout(() => {
          console.log("Async operation succeeded with result:", result);
        }, 2000);        
        // Further asynchronous operation can be chained here
        return result * 2; // For example, double the result
    })
    .then(doubleResult => {
        console.log("Doubled result:", doubleResult);
        // Another chained operation can be performed here
    })
    .catch(error => {
        console.error("Async operation failed with error:", error.message);
        // Handle the error gracefully
    }); -->

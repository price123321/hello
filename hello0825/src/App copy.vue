<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'

// export default {
//   data() {
//     return {
//       count: 1
//     }
//   },
//   mounted() {
//     // `this` refers to the component instance.
//     console.log(this.count) // => 1

//     // data can be mutated as well
//     this.count = 2
//   }
// }

// import { ref, onMounted } from 'vue'

// // reactive state
// const count = ref(0)

// // functions that mutate state and trigger updates
// function increment() {
//   count.value++
// }


// onMounted(() => {
//   console.log(`The initial count is ${count.value}.`)
// })
console.log('dddd')
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
      <!-- <div id="app1"><button @click="count++">{{ count }}</button></div> -->
    </div>
  </header>

  <main>
    <TheWelcome />
    <!-- <div id="app1"><button @click="count++">{{ count }}</button></div>    -->
  </main>
  <!-- <button @click="increment">Count is: {{ count }}</button> -->
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>

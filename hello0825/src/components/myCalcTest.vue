<script setup>

import { ref, onMounted } from 'vue';
const eInput= ref(null);
const piInput= ref(null);
const eValue =  ref(null);
const piValue = ref(null);

 onMounted(() => {
    //   console.log(myElement.value); // Access the DOM element
    //   myElement.value.textContent = "New content!";
     console.log(eInput);
    console.log(eInput.value);

this.$refs.e-slider-ref.addEventListener("input", function () {
  e.style.transform = `rotate(calc(1deg * pow(${this.value}, e)))`;
  eValue.textContent = e.style.transform;
});

piInput.addEventListener("input", function () {
  pi.style.rotate = `calc(sin(${this.value} * pi) * 100deg)`;
  piValue.textContent = pi.style.rotate;
});

    });

// sliders
// const eInput = document.querySelector("#e-slider");
// const piInput = document.querySelector("#pi-slider");
// spans for displaying values
// const eValue = document.querySelector("#e-value");
// const piValue = document.querySelector("#pi-value");


</script>

<template>
<div id="wrapper">
  <div class="container">
    <div id="e"></div>
    <input ref="e-slider-ref" type="range" min="0" max="7" step="0.01" value="0" id="e-slider" />
    <label for="e-slider">e:</label>
    <span id="e-value"></span>
  </div>
  <div class="container">
    <div id="pi"></div>
    <input type="range" min="0" max="1" step="0.01" value="0" id="pi-slider" />
    <label for="pi-slider">pi:</label>
    <span id="pi-value"></span>
  </div>
</div>
</template>


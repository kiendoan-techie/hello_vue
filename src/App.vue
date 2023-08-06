<script setup>
import { ref } from 'vue'

// attribute binding
const titleClass = ref('title')

// event binding
const count = ref(0)
function increment() {
  count.value++
}

// form binding
const text = ref('')
function onInput(e) {
  text.value = e.target.value
}

// conditional binding
const awesome = ref(true)
function toggle() {
  // ...
}

</script>

<template>
  <h1 :class="titleClass"> Attribute binding: Make me red</h1>	<p></p>

  <h1> Event binding </h1>	<p></p>
  <button @click="increment">count is: {{ count }}</button>	<p></p>

  <h1> Form binding </h1>	<p></p>
  <input :value="text" @input="onInput" placeholder="Type here">	<p></p>
  <p>{{ text }}</p>	<p></p>

  <h1> Conditional binding</h1>	<p></p>
  <button @click="awesome = !awesome">toggle</button>	<p></p>
  <h1 v-if="awesome">Vue is awesome!</h1>
  <h1 v-else>Oh no 😢</h1>



</template>

<style>
.title {
  color: red;
}
</style>

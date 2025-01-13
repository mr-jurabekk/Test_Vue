<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      You’ve successfully created a project with
      <button :disabled="isButtonDisabled">Button</button>


      <div
          class="static"
          :class="{ active: isActive, 'text-danger': hasError }"
      >Hello</div>
      <a href="https://vite.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
    </h3>
  </div>
</template>

<script lang="ts" setup>

import {ref} from "vue";
defineProps({
  msg: {
    type: String,
    required: true,
  },
})
const isButtonDisabled = ref(true);
const isActive = ref(true)
const hasError = ref(false)


</script>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>

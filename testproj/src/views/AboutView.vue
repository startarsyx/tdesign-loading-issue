<template>
  <div class="about">
    <h1 v-loading="loadingFlag">This is an about page</h1>
    <button @click="testLoading"> test loading </button>
  </div>
</template>

<script setup>

import {ref} from 'vue'

const loadingFlag = ref(false);

const testLoading = () => {
  loadingFlag.value = true;
  setTimeout(() => {
    loadingFlag.value = false;
  }, 500);
}

</script>

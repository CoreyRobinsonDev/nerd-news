<script setup lang="ts">
import Story from './Story.vue';

const res = await fetch("https://hacker-news.firebaseio.com/v0/topstories.json?print=pretty");
const data = await res.json();
</script>

<template>
  <Story v-for="value in data" :key="value" :id="value" />
</template>

<style scoped>
</style>
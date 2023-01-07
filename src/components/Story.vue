<script setup lang="ts">
const { id } = defineProps({
  id: Number
})

const res = await fetch(`https://hacker-news.firebaseio.com/v0/item/${id}.json?print=pretty`);
const {title, by, kids, score, time} = await res.json();



</script>

<template>
  <article>
    <header>
      <p>By: {{ by }}</p>
      <p>{{ score }}</p>
    </header>
    <main>
      <h2>{{ title }}</h2>
    </main>
  </article>
</template>

<style scoped>
</style>
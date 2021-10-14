<template>
  <NuxtLink
    class="bg-purple-200 p-4 rounded border-2 border-purple-400"
    :to="`products/${card.id}`"
  >
    <h3 class="text-lg font-bold mb-2">{{ card.title }}</h3>
    <p class="text-base">{{ card.snippet }}</p>
  </NuxtLink>
</template>

<script>
export default {
  props: ['card'],
};
</script>

<template>
  <section class="py-4">
    <h4 class="text-2xl font-bold">{{ cardsSection.title }}</h4>
    <p class="text-xl">{{ cardsSection.snippet }}</p>
    <div class="py-2 grid grid-flow-col gap-3">
      <LargeCard
        v-for="card in cardsSection.cards"
        :key="card.id"
        :card="card"
      />
    </div>
  </section>
</template>

<script>
export default {
  props: ['cardsSection'],
};
</script>

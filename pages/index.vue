<template>
  <div class="min-h-screen w-screen bg-purple-100">
    <Nav />
    <main class="m-auto max-w-prose p-10">
      <Hero class="mb-14" />
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo"
        :key="cardInfo.id"
        :cards-section="cardInfo"
      />
    </main>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import { largeCardSections } from '@/assets/data';

export default Vue.extend({
  data() {
    return {
      largeCardInfo: largeCardSections,
    };
  },
});
</script>

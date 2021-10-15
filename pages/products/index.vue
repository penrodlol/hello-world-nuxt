<template>
  <div class="min-h-screen w-screen bg-purple-100">
    <main class="m-auto max-w-prose p-10">
      <h1
        class="
          text-5xl
          mb-4
          font-extrabold
          text-transparent
          bg-clip-text bg-gradient-to-br
          from-blue-400
          to-purple-600
        "
      >
        Products
      </h1>
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo.slice(0, 1)"
        :key="cardInfo.id"
        :cards-section="cardInfo"
      />
    </main>
  </div>
</template>

<script>
import { largeCardSections } from '@/assets/data';

export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
    };
  },
};
</script>

<template>
  <div class="px-10 py-4 bg-purple-100 rounded border-2 border-purple-400">
    <h1 class="text-3xl">
      {{ rental.title }}
    </h1>
    <p class="text-base mb-6">{{ rental.snippet }}</p>
    <button
      class="float-right text-red-700 font-bold text-base"
      @click="() => removeItem(rental.id)"
    >
      Remove
    </button>
  </div>
</template>

<script>
import { mapMutations } from 'vuex';

export default {
  props: ['rental'],
  methods: {
    ...mapMutations(['removeItem']),
  },
};
</script>

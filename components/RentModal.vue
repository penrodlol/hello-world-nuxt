<template>
  <button
    class="
      bg-purple-300
      rounded
      px-6
      py-4
      hover:bg-purple-400
      font-bold
      cursor-pointer
      shadow-md
      w-full
      text-xl
    "
    @click="() => addItem(id)"
  >
    Rent
  </button>
</template>

<script>
import { mapMutations } from 'vuex';

export default {
  props: ['id'],
  methods: {
    ...mapMutations(['addItem']),
  },
};
</script>

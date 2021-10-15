<template>
  <section>
    <h1
      class="
        my-6
        text-5xl
        mb-10
        font-extrabold
        text-transparent
        bg-clip-text bg-gradient-to-br
        from-blue-400
        to-purple-600
      "
    >
      Rentals
    </h1>
    <div class="grid gap-4">
      <MyItem v-for="rental in myRentals" :key="rental.id" :rental="rental" />
    </div>
  </section>
</template>

<script>
import { mapState } from 'vuex';

export default {
  layout: 'no-nav',
  computed: {
    ...mapState(['myRentals']),
  },
};
</script>

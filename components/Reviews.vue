<template>
  <section>
    <h3 class="text-2xl font-semibold text-blue-600 mb-6">Customer Reviews</h3>
    <div v-if="!$fetchState.pending">
      <div class="grid gap-5">
        <ReviewCard
          v-for="reviewer in reviewers.results"
          :key="reviewer.login.uuid"
          :reviewer="reviewer"
        />
      </div>
    </div>
    <div v-else>Loading...</div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      reviewers: [],
    };
  },
  async fetch() {
    const url = 'https://randomuser.me/api/?results=5';
    this.reviewers = await fetch(url).then((res) => res.json());
  },
};
</script>

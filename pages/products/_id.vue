<template>
  <div>
    <main
      class="
        m-auto
        mt-10
        max-w-prose
        p-10
        bg-purple-200
        rounded
        border-2 border-purple-400
      "
    >
      <div v-if="product">
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
          {{ product.title }}
        </h1>
        <p class="text-base">{{ product.snippet }}</p>
        <RentModal :id="product.id" class="my-5" />
        <hr class="my-5 border-2 border-blue-500 rounded" />
        <p class="text-base">{{ product.description }}</p>
        <hr class="my-10 border-2 border-blue-500 rounded" />
        <Reviews />
      </div>
      <div v-else>
        <PageNotFound />
      </div>
    </main>
  </div>
</template>

<script>
export default {
  computed: {
    product() {
      const route = Number(this.$route.params.id);
      return this.$store.getters.getProductById(route);
    },
  },
};
</script>

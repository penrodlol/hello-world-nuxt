<template>
  <nav class="shadow-md p-4 bg-blue-200">
    <div
      class="
        max-w-screen-xl
        m-auto
        grid grid-flow-col
        items-center
        justify-between
      "
    >
      <NuxtLink
        class="text-3xl font-bold cursor-pointer hover:text-purple-400"
        to="/"
      >
        Nuxt
      </NuxtLink>
      <div class="text-xl">
        <NuxtLink
          class="mr-4 cursor-pointer hover:text-purple-400"
          to="products"
        >
          Products
        </NuxtLink>
        <NuxtLink class="cursor-pointer hover:text-purple-400" to="items">
          Items
        </NuxtLink>
      </div>
    </div>
  </nav>
</template>

<script>
export default {};
</script>

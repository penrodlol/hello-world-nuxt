<template>
  <div class="p-4 border-2 border-purple-400 rounded shadow-md">
    <h6 class="font-bold mb-2">@{{ reviewer.login.username }}</h6>
    <p class="text-sm">
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Modi vero
      aliquid corrupti ipsa! Beatae laudantium alias tempora. Dolor cumque
      placeat blanditiis, veritatis vitae reprehenderit distinctio voluptate
      accusantium aliquid provident et!
    </p>
  </div>
</template>

<script>
export default {
  props: ['reviewer'],
};
</script>

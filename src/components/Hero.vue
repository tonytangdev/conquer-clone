<template>
  <div class="relative bg-red-500 pb-11/12">
    <img
      class="absolute h-full w-full object-cover"
      :src="img.imageUrl"
      :alt="img.imageAlt"
    />
    <div
      class="absolute text-white text-center m-auto right-0 left-0 top-1/5 font-sans"
    >
      <h1 class="text-6xl text-shadow-2">CONQUER</h1>
      <h2 class="text-2xl text-shadow-1">Simple VueJS Template</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Hero',
  data: () => ({
    img: {
      imageUrl: require('../assets/img/bg-1.jpg'),
      imageAlt: 'hero image'
    }
  })
};
</script>

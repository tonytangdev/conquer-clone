<template>
  <div class="flex-col bg-gray-200 mb-6 pb-5 text-center">
    <img v-if="card.img" :src="card.img.imageUrl" :alt="card.img.imageAlt" />
    <div class="text-center px-5">
      <h3 class="text-2xl font-bold my-3" :class="card.title.class">
        {{ card.title.text }}
      </h3>
      <p v-for="p in card.content" :key="p.id" class="mb-5 font-sans">
        {{ p.text }}
      </p>
      <button
        v-if="card.button"
        class="px-8 py-2 text-white font-semibold text-xl rounded-md"
        :class="card.button.class"
      >
        {{ card.button.text }}
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'card',
  props: ['card']
};
</script>

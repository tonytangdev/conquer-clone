<template>
  <div
    class="flex-col bg-gray-200 mb-6 pb-5 text-center object-cover bg-center content-center flex"
    :style="`background-image: url(${cardImg.img.imageUrl}); height: 433px;`"
  >
    <div class="text-center px-5 m-auto">
      <h3 class="text-2xl font-bold my-3" :class="cardImg.title.class">
        {{ cardImg.title.text }}
      </h3>
      <p
        v-for="p in cardImg.content"
        :key="p.id"
        class="mb-5 font-sans text-white"
      >
        {{ p.text }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'cardImg',
  props: ['card-img']
};
</script>

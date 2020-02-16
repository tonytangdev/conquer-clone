<template>
  <nav class="fixed w-full top-0">
    <button
      @click="showMenu"
      class="z-10 right-1/12 top-1/12 border-gray-900 border-2 rounded-md px-3 py-1 text-white bg-gray-800"
    >
      <font-awesome-icon :icon="['fas', 'bars']" />
    </button>
    <div
      v-show="mouseOverBtn"
      class="bg-gray-700 text-white mt-2 shadow-md py-1 text-center right-0 z-10 w-full"
    >
      <a
        v-for="item in items"
        :key="item.id"
        :href="item.href"
        class="block px-4 py-1"
      >
        {{ item.name }}
      </a>
    </div>
    <Hero />
  </nav>
</template>

<script>
import Hero from './Hero.vue';

export default {
  name: 'navbar',
  data: () => ({
    mouseOverBtn: false,
    items: [
      {
        id: 1,
        name: 'Homepage',
        href: '#'
      },
      {
        id: 2,
        name: 'About us',
        href: '#'
      },
      {
        id: 3,
        name: 'Services',
        href: '#'
      },
      {
        id: 4,
        name: 'Contact',
        href: '#'
      },
      {
        id: 5,
        name: 'External',
        href: '#'
      }
    ]
  }),
  methods: {
    showMenu: function() {
      this.mouseOverBtn = !this.mouseOverBtn;
    }
  },
  components: {
    Hero
  }
};
</script>

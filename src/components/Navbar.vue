<template>
  <nav class="fixed w-full top-0 z-10">
    <div
      class="w-full container mx-auto flex flex-wrap items-end mt-0 py-2 flex-col"
    >
      <div class="block pr-4">
        <button
          @click="showMenu"
          class="border-gray-900 border-2 rounded-md px-3 py-2 text-white bg-gray-800 flex items-center"
        >
          <font-awesome-icon :icon="['fas', 'bars']" />
        </button>
      </div>
    </div>
    <div
      v-show="mouseOverBtn"
      class="bg-gray-700 text-white shadow-md py-1 text-center mx-2"
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
  </nav>
</template>

<script>
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
  }
};
</script>

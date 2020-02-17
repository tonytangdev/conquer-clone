<template>
  <div id="app">
    <Navbar />
    <Hero />
    <div class="px-4 mt-20">
      <Card v-for="card in cards1" :key="card.id" :card="card" />
      Autres
      <Card v-for="card in cards2" :key="card.title" :card="card" />
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import Card from './components/Card.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Hero,
    Card
  },
  data: () => ({
    cards1: [
      {
        id: 1,
        img: {
          imageUrl: require('./assets/img/1-1.jpg'),
          imageAlt: 'bootstrap'
        },
        title: {
          text: 'Bootstrap v3.3.6',
          class: 'text-green-600'
        },
        content: [
          {
            id: 1,
            text:
              'Morbi sagittis justo a velit placerat ullamcorper quis quis velit. Sed convallis at risus ullamcorper auctor. Praesent quis velit neque. Quisque semper porta nisi vitae suscipit. Duis lectus magna, ornare ac scelerisque.'
          }
        ],
        button: {
          text: 'Green Button',
          class: 'bg-green-600'
        }
      },
      {
        id: 2,
        img: {
          imageUrl: require('./assets/img/1-2.jpg'),
          imageAlt: 'responsive'
        },
        title: {
          text: 'Responsive Design',
          class: 'text-blue-600'
        },
        content: [
          {
            id: 1,
            text:
              'Conquer Template is provided by templatemo for free of charge. You can use this template for any kind of website. No credit link is required. All images by Unsplash. Thank you for visiting our website. Please come again!'
          }
        ],
        button: {
          text: 'See Details',
          class: 'bg-blue-600'
        }
      },
      {
        id: 3,
        img: {
          imageUrl: require('./assets/img/1-3.jpg'),
          imageAlt: 'parallax'
        },
        title: {
          text: 'Parallax Layout',
          class: 'text-red-600'
        },
        content: [
          {
            id: 1,
            text:
              'Morbi sagittis justo a velit placerat ullamcorper quis quis velit. Sed convallis at risus ullamcorper auctor. Praesent quis velit neque. Quisque semper porta nisi vitae suscipit. Duis lectus magna, ornare ac scelerisque.'
          }
        ],
        button: {
          text: 'Button Red',
          class: 'bg-red-600'
        }
      },
      {
        id: 4,
        img: {
          imageUrl: require('./assets/img/2-1.jpg'),
          imageAlt: 'two columns'
        },
        title: {
          text: 'Two Column Left Side',
          class: 'text-gray-700'
        },
        content: [
          {
            id: 1,
            text:
              'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam tempor eros eget eros maximus, ut cursus sem euismod. Donec iaculis tristique odio at consectetur. Nullam dignissim varius suscipit. Sed in leo sit amet velit finibus pretium.'
          },
          {
            id: 2,
            text:
              'Vestibulum vel mauris at erat mattis accumsan et ac lorem. Cras non venenatis orci, sed tincidunt massa. Duis nisl lectus, auctor eu sodales at, dignissim eu orci. Sed vitae venenatis magna, in blandit metus.'
          }
        ]
      },
      {
        id: 5,
        img: {
          imageUrl: require('./assets/img/2-2.jpg'),
          imageAlt: 'two columns'
        },
        title: {
          text: 'Two Column Right Side',
          class: 'text-gray-700'
        },
        content: [
          {
            id: 1,
            text:
              'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam tempor eros eget eros maximus, ut cursus sem euismod. Donec iaculis tristique odio at consectetur. Nullam dignissim varius suscipit. Sed in leo sit amet velit finibus pretium.'
          },
          {
            id: 2,
            text:
              'Vestibulum vel mauris at erat mattis accumsan et ac lorem. Cras non venenatis orci, sed tincidunt massa. Duis nisl lectus, auctor eu sodales at, dignissim eu orci. Sed vitae venenatis magna, in blandit metus.'
          }
        ],
        button: {
          text: 'Read More',
          class:
            'bg-white text-gray-700 border border-solid border-2 border-gray-500'
        }
      },
      {
        id: 6,
        title: {
          text: 'Two Column Left Side',
          class: 'text-gray-700'
        },
        content: [
          {
            id: 1,
            text:
              'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam tempor eros eget eros maximus, ut cursus sem euismod. Donec iaculis tristique odio at consectetur. Nullam dignissim varius suscipit. Sed in leo sit amet velit finibus pretium.'
          },
          {
            id: 2,
            text:
              'Vestibulum vel mauris at erat mattis accumsan et ac lorem. Cras non venenatis orci, sed tincidunt massa. Duis nisl lectus, auctor eu sodales at, dignissim eu orci. Sed vitae venenatis magna, in blandit metus.'
          }
        ]
      }
    ]
  })
};
</script>

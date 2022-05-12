<template>
  <top-nav/>
  <div class="px-20 w-full flex flex-wrap">
    <div v-for="(arr, index) in subArrays" :key="index" class="w-1/5">
      <div v-for="(card, i) in arr" :key="i" class="w-full" >
        <div class="w-full p-2">
          <CardItem :src="`${card.src}`" :board="`${card.recommended}`" class="w-full h-full" />
          <div class="text-sm leading-tight pt-2">
            <p class="font-bold">{{card.title}}</p>
            <p>{{card.user}}</p>
          </div>
        </div>
    </div>
    </div>
  </div>
  
</template>

<script>
import TopNav from './components/TopNav.vue';
import CardItem from './components/CardItem.vue';

export default {
  name: 'App',
  components: {
    TopNav,
    CardItem
  },
  computed: {
    subArrays() {
      let length = Math.ceil(this.cards.length / 5);
      const result = new Array(length)
        .fill()
        .map((i) => {
          console.log(i)
          return this.cards.splice(0, length)
        })
      return result
    }
  },
  data(){
    return {
      cards: [
        {
          src: '1.jpg',
          title: 'Title 1',
          user: 'User 1',
          recommended: 'Naruto'
        },
                {
          src: '2.jpg',
          title: 'Title 2',
          user: 'User 2',
          recommended: 'Naruto'
        },
                {
          src: '3.jpg',
          title: 'Title 3',
          user: 'User 3',
          recommended: 'Naruto'
        },
                {
          src: '4.png',
          title: 'Title 4',
          user: 'User 4',
          recommended: 'Naruto'
        },
                {
          src: '5.jpg',
          title: 'Title 5',
          user: 'User 5',
          recommended: 'Naruto'
        },
                {
          src: '1.jpg',
          title: 'Title 1',
          user: 'User 1',
          recommended: 'Naruto'
        },
                {
          src: '2.jpg',
          title: 'Title 2',
          user: 'User 2',
          recommended: 'Naruto'
        },
                {
          src: '3.jpg',
          title: 'Title 3',
          user: 'User 3',
          recommended: 'Naruto'
        },
                {
          src: '4.png',
          title: 'Title 4',
          user: 'User 4',
          recommended: 'Naruto'
        },
                {
          src: '5.jpg',
          title: 'Title 5',
          user: 'User 5',
          recommended: 'Naruto'
        },
                {
          src: '1.jpg',
          title: 'Title 1',
          user: 'User 1',
          recommended: 'Naruto'
        },
                {
          src: '2.jpg',
          title: 'Title 2',
          user: 'User 2',
          recommended: 'Naruto'
        },
                {
          src: '3.jpg',
          title: 'Title 3',
          user: 'User 3',
          recommended: 'Naruto'
        },
                {
          src: '4.png',
          title: 'Title 4',
          user: 'User 4',
          recommended: 'Naruto'
        },
                {
          src: '5.jpg',
          title: 'Title 5',
          user: 'User 5',
          recommended: 'Naruto'
        },
                {
          src: '1.jpg',
          title: 'Title 1',
          user: 'User 1',
          recommended: 'Naruto'
        },
                {
          src: '2.jpg',
          title: 'Title 2',
          user: 'User 2',
          recommended: 'Naruto'
        },
                {
          src: '3.jpg',
          title: 'Title 3',
          user: 'User 3',
          recommended: 'Naruto'
        },
                {
          src: '4.png',
          title: 'Title 4',
          user: 'User 4',
          recommended: 'Naruto'
        },
                {
          src: '5.jpg',
          title: 'Title 5',
          user: 'User 5',
          recommended: 'Naruto'
        },
                {
          src: '1.jpg',
          title: 'Title 1',
          user: 'User 1',
          recommended: 'Naruto'
        },
                {
          src: '2.jpg',
          title: 'Title 2',
          user: 'User 2',
          recommended: 'Naruto'
        },
                {
          src: '3.jpg',
          title: 'Title 3',
          user: 'User 3',
          recommended: 'Naruto'
        },
                {
          src: '4.png',
          title: 'Title 4',
          user: 'User 4',
          recommended: 'Naruto'
        },
                {
          src: '5.jpg',
          title: 'Title 5',
          user: 'User 5',
          recommended: 'Naruto'
        }
      ]
    }
  }
}
</script>

<style>

</style>

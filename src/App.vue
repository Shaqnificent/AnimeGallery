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
          src: '6.jpg',
          title: 'Title 1',
          user: 'User 1',
          recommended: 'Naruto'
        },
                {
          src: '7.png',
          title: 'Title 2',
          user: 'User 2',
          recommended: 'Naruto'
        },
                {
          src: '8.jpg',
          title: 'Title 3',
          user: 'User 3',
          recommended: 'DBZ'
        },
                {
          src: '9.png',
          title: 'Title 4',
          user: 'User 4',
          recommended: 'DBZ'
        },
                {
          src: '10.jpg',
          title: 'Title 5',
          user: 'User 5',
          recommended: 'DBZ'
        },
                {
          src: '11.jpg',
          title: 'Title 11',
          user: 'User 11',
          recommended: 'DBZ'
        },
                {
          src: '12.jpg',
          title: 'Title 12',
          user: 'User 12',
          recommended: 'Haikyuu'
        },
                {
          src: '13.jpg',
          title: 'Title 13',
          user: 'User 13',
          recommended: 'Haikyuu'
        },
                {
          src: '14.png',
          title: 'Title 14',
          user: 'User 14',
          recommended: 'Haikyuu'
        },
                {
          src: '15.jpg',
          title: 'Title 15',
          user: 'User 15',
          recommended: 'Bleach'
        },
                {
          src: '16.jpg',
          title: 'Title 16',
          user: 'User 16',
          recommended: 'Bleach'
        },
                {
          src: '17.png',
          title: 'Title 17',
          user: 'User 17',
          recommended: 'Bleach'
        },
                {
          src: '18.jpg',
          title: 'Title 18',
          user: 'User 18',
          recommended: 'Bleach'
        },
                {
          src: '19.png',
          title: 'Title 19',
          user: 'User 19',
          recommended: 'Bleach'
        },
                {
          src: '20.jpg',
          title: 'Title 20',
          user: 'User 20',
          recommended: 'JJK'
        },
                {
          src: '21.jpg',
          title: 'Title 21',
          user: 'User 21',
          recommended: 'Black Clover'
        },
                {
          src: '22.jpg',
          title: 'Title 22',
          user: 'User 22',
          recommended: 'Black clover'
        },
                {
          src: '23.jpg',
          title: 'Title 23',
          user: 'User 23',
          recommended: 'Fairy Tail'
        },
                {
          src: '24.png',
          title: 'Title 24',
          user: 'User 24',
          recommended: 'Fairy Tail'
        },
                {
          src: '25.jpg',
          title: 'Title 25',
          user: 'User 25',
          recommended: 'Demon Slayer'
        }
      ]
    }
  }
}
</script>

<style>

</style>

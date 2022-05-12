<template>
  <top-nav/>
  <div class="px-20">
    <div class="w-1/5">
    <CardItem src="1.jpg"  class="w-full h-full" />
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
  }
}
</script>

<style>

</style>

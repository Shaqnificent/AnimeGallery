<template lang="html">
    <div class="px-3 py-4 flex items-center justify-between">
        <div class="flex items-center">
            <button class="rounded-full hover:bg-light p-3 flex items-center justify-center" type="button" name="button">
                <img src="logo.png" alt="" class="h-6 w-6 rounded-full">
            </button>
            <button v-for="(item, i) in tabItems" :key="i" @click="selectedTab = item.key" :class="`${selectedTab=== item.key ? 'bg-dark text-white': 'text-dark hover:bg-light font-semibold'} rounded-full py-3 px-4`" type="button" name="button">
                {{item.name}}
            </button>
        </div>
        <div class="flex-grow relative">
            <span class="material-icons absolute mt-3 ml-3 text-muted">search</span>
            <input class="hover:bg-lightHover w-full rounded-full bg-light py-3 pr-3 pl-10" placeholder="Search" type="text" name="" values="">
        </div>
        <div class="flex items-center">
            <button type="button" name="button" class="relative rounded-full items-center flex hover:bg-light justify-center p-3"> 
                <span class="material-icons text-3xl">notifications</span> 
                <div class="rounded-full h-5 w-5 bg-primary text-white flex items-center justify-center absolute mb-5 ml-5">4</div>
            </button>
            <button type="button" name="button" class="relative rounded-full items-center flex hover:bg-light justify-center p-3"> 
                <span class="material-icons text-3xl">textsms</span> 
                <div class="rounded-full h-5 w-5 bg-primary text-white flex items-center justify-center absolute mb-5 ml-5">1</div>
            </button>
            <button class="rounded-full hover:bg-light p-3 flex items-center justify-center" type="button" name="button">
                <div class="w-6 h-6 bg-center bg-cover rounded-full" style="background-image: url(profile.jpg)"></div>
            </button>
            <button type="button" name="button" class="w-6 h-6 hover:bg-light rounded-full flex items-center justify-center">
                 <span class="material-icons">expand_more</span> 
            </button>
        </div>
    </div>
</template>

<script>
export default {
    setup() {
        
    },
    data(){
        return {
            tabItems: [
                {name: 'Home', key: 'home'},
                {name: 'Today', key: 'today'},
            ],
            selectedTab: 'home'
        }
    }
}
</script>
<style scoped>

</style>
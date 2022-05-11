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
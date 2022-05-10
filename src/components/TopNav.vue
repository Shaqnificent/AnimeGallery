<template lang="html">
    <div class="p-3 flex items-center justify-between">
        <div class="flex items-center">
            <button class="rounded-full hover:bg-light p-3 flex items-center justify-center" type="button" name="button">
                <img src="logo.png" alt="" class="h-6 w-6 rounded-full">
            </button>
            <button v-for="(item, i) in tabItems" :key="i" @click="selectedTab = item.key" :class="`${selectedTab=== item.key ? 'bg-dark text-white': 'text-dark hover:bg-light font-semibold'} rounded-full py-3 px-5`" type="button" name="button">
                {{item.name}}
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
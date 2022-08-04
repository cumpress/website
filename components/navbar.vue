<template>
    <nav class="w-full flex items-center justify-center bg-gray-800 bg-opacity-50 backdrop-blur-sm fixed z-50">
        <div class="w-full lg:w-2/3 py-6 px-6 flex flex-col gap-10 lg:flex-row items-center justify-between">
            <div class="flex flex-row items-center justify-between w-full lg:w-auto">
                <nuxt-link to="/"><h1 class="text-2xl font-bold">Cumpress</h1></nuxt-link>
                <span class="cursor-pointer lg:hidden" @click="nav = !nav">X</span>
            </div>
            <div v-if="nav" class="flex flex-col lg:flex-row items-center gap-5">
                <nuxt-link class="trans-btn" to="/#docs">Quick start.</nuxt-link>
                <nuxt-link class="trans-btn" to="/docs">Docs.</nuxt-link>
                <nuxt-link class="trans-btn" to="/speed">Speed.</nuxt-link>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    name:'navbar',
    data:() => {
        return{
            nav:true
        }
    }
}
</script>
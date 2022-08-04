<template>
    <section class="w-full flex items-center justify-center h-full gap-4">
        <div class="w-full lg:w-2/3 flex flex-col items-center justify-center h-full">
            <h1 class="text-4xl font-bold mb-4">Speed tests.</h1>

            <div class="flex flex-col w-full gap-4">
                <h1 class="text-2xl font-bold">Cumpress</h1>
                <span>0,099 ms</span>
                <span :style="'width: '+cum+'%'" class="w-full h-1 bg-green-600 rounded-full duration-300"></span>
            </div>

            <span class="hr"></span>

            <div class="flex flex-col w-full gap-4">
                <h1 class="text-2xl font-bold">Fastify</h1>
                <span>0,791 ms</span>
                <span :style="'width: '+fast+'%'" class="w-full h-1 bg-green-600 rounded-full duration-300"></span>
            </div>

            <span class="hr"></span>

            <div class="flex flex-col w-full gap-4">
                <h1 class="text-2xl font-bold">Express</h1>
                <span>0,951 ms</span>
                <span :style="'width: '+exp+'%'" class="w-full h-1 bg-green-600 rounded-full duration-300"></span>
            </div>
        </div>
        <script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/11.6.0/highlight.min.js"></script>
        <script>hljs.highlightAll();</script>
    </section>
</template>

<script>
export default {
  name: 'speed',
  created(){
    setTimeout(() => {
        this.cum = 100;
        this.fast = 30;
        this.exp = 15;
    }, 500);
  },
  data:() => {
    return{
        cum:0,
        fast:0,
        exp:0
    }
  }
}
</script>

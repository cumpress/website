<template>
    <section v-if="error" class="w-full flex flex-col items-center justify-center h-full">
      <div class="py-6 px-6 bg-red-100 text-red-600 flex flex-col items-center gap-4 rounded-lg">
        <h1 class="text-4xl font-bold">{{error.path}} - {{error.statusCode}}</h1>
        <span>{{error.message}}</span>
      </div>
    </section>
</template>

<script>
  export default {
    props: ['error'],
    layout: 'error'
  }
</script>
<script setup>
  defineProps({
    title:{
      type: String,
      default: "Title",
    },
    image: {
      type: Object,
      default(){
        return{
          src: "product name",
          alt: "img info",
        };
      },
    },
    url:{
      type: String,
      default: "#",
    },
    buttonColor:{
      type: String,
      default: "bg-slate-500"
    }
  });
</script>

<template>
  <article class="max-w-sm bg-slate-100 p-4 text-center ml-5 drop-shadow-md">
    <div>
      <h3 class="text-2xl">{{title}}</h3>
    </div>
    <div class="flex flex-column">
      <img :src="image.src" :alt="image.alt" class="w-full h-48 object-cover"/>
    </div>
    <div>
      <NuxtLink :to="url" :class="buttonColor" class="block bg-slate-500 rounded-md mx-auto py-1 mt-5  hover:scale-105">Buy now!</NuxtLink>
    </div>
  </article>
</template>
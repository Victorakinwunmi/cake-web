<template>
  <div class="">
    <div class="group">
      <div class="border cursor-pointer border-transparent transition group-hover:bg-white duration-700 ease-in-out group-hover:border-pink-500 pt-10 pb-10 group-hover:pb-44 px-0 rounded-full">
        <img :src="pic" class="w-44 mx-auto" />
        <div class="mb-16">
          <h1 class="text-center font-bold text-xl lg:text-2xl">
            {{ title }}
          </h1>
          <p class="text-center mt-4 max-w-sm md:max-w-md px-8 mx-auto">{{ desc }}</p>
        </div>
        <button class="w-full flex items-center transition duration-700 ease-in-out opacity-0 group-hover:opacity-100 justify-center">
          <h1 class="font-black">Buy now</h1>
          <img :src="require('@/assets/icons/Right.png')" class="w-4 mx-2">
        </button>
        
      </div>
       
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    desc: String,
    pic: String,
  },
};
</script>

<style>
</style>
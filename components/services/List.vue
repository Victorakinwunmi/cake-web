<template>
  <div class="shadow-xl bg-pink-100 mt-10 rounded-3xl">
    <div class="block lg:flex justify-center items-center mt-3">
      <div class="">
        <h1 class="text-black font-bold">{{ title }}</h1>
        <button
          class="flex justify-between items-center border border-black p-2 mt-4"
        >
          <div class="text-black text-base">Learn More</div>
          <img :src="require('@/assets/icons/Right.png')" class="w-4 ml-2" />
        </button>
      </div>
      <div class="ml-4">
        <div class="block w-44 rounded-full mx-auto overflow-hidden">
          <img :src="pic" class="w-full object-cover" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    btn: String,
    pic: String,
  },
};
</script>

<style>
</style>
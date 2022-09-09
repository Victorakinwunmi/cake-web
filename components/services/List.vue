<template>
  <div class="px-4 py-2 shadow-xl bg-gradient-to-t from-pink-200 to-pink-100 mt-10 rounded-3xl">
    <div class="flex justify-center items-center mt-3">
      <div class="">
        <h1 class="text-black font-bold">{{ title }}</h1>
        <button
          class="flex justify-between items-center border border-black p-2 mt-4"
        >
          <div class="text-black text-base">Learn More</div>
          <img :src="require('@/assets/icons/Right.png')" class="w-4 ml-2" />
        </button>
      </div>
      <div class="ml-2 md:ml-4">
        <div class="block w-44 rounded-full mx-auto overflow-hidden">
          <img :src="pic" class="w-11/12 object-cover" />
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
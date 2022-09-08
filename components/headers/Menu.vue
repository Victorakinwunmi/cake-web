<template>
  <div>
    <div class="lg:flex text-black font-semibold">
      <nuxt-link to="/" class="block mt-10 mb-1 w-12 lg:w-full mx-8 lg:mx-4 lg:py-1 lg:mt-0 lg:mb-0 hover:text-pink-600 border-b-4 hover:border-pink-600 border-transparent duration-500 ease-in-out"><slot name="hometext" /></nuxt-link>
      <nuxt-link to="service" class="block mt-5 mb-1 w-12 mx-8 lg:w-full lg:mx-4 lg:py-1 lg:mt-0 lg:mb-0 hover:text-pink-600 hover:text-pink-600 border-b-4 hover:border-pink-600 border-transparent duration-500 ease-in-out" ><slot name="servicetext" /></nuxt-link>
      <nuxt-link to="menupage" class="block mt-5 mb-1 w-12 mx-8 lg:w-full lg:mx-4 lg:py-1 lg:mt-0 lg:mb-0 hover:text-pink-600 hover:text-pink-600 border-b-4 hover:border-pink-600 border-transparent duration-500 ease-in-out"><slot name="menutext" /></nuxt-link>
      <nuxt-link to="contact" class="block mt-5 mb-1 w-12 mx-8 lg:w-full lg:mx-4 lg:py-1 lg:mt-0 lg:mb-0 hover:text-pink-600 hover:text-pink-600 border-b-4 hover:border-pink-600 border-transparent duration-500 ease-in-out"><slot name="contacttext" /></nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
 
};
</script>

<style>
</style>
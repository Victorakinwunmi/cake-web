<template>
  <div>
    <div class="lg:flex text-black font-semibold">
      <nuxt-link to="www.pahh.com" class="block mt-10 mb-1  mx-8 lg:mx-4 lg:py-1 lg:mt-0 lg:mb-0 hover:text-pink-600 border-b-4 hover:border-pink-600 border-transparent duration-500 ease-in-out"><slot name="hometext" /></nuxt-link>
      <nuxt-link to="www.paath" class="block mt-5 mb-1  mx-8 lg:mx-4 lg:py-1 lg:mt-0 lg:mb-0 hover:text-pink-600 hover:text-pink-600 border-b-4 hover:border-pink-600 border-transparent duration-500 ease-in-out" ><slot name="servicetext" /></nuxt-link>
      <nuxt-link to="www.pptth.com" class="block mt-5 mb-1  mx-8 lg:mx-4 lg:py-1 lg:mt-0 lg:mb-0 hover:text-pink-600 hover:text-pink-600 border-b-4 hover:border-pink-600 border-transparent duration-500 ease-in-out"><slot name="menutext" /></nuxt-link>
      <nuxt-link to="www.paath.com" class="block mt-5 mb-1  mx-8 lg:mx-4 lg:py-1 lg:mt-0 lg:mb-0 hover:text-pink-600 hover:text-pink-600 border-b-4 hover:border-pink-600 border-transparent duration-500 ease-in-out"><slot name="contacttext" /></nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
 
};
</script>

<style>
</style>
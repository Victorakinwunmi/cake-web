<template>
  <div class="flex items-center+">
     <input type="search" placeholder="What are you looking for?" :class="show? 'p-2 bg-transparent outline-none border border-black rounded-full w-56':'hidden'">
    <button>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        class="w-7 h-7 fill-current lg:mx-4 hover:text-pink-600 ml-3 lg:ml-0"
        viewBox="0 0 50 50"
        version="1.1"
        @click="showSearch"
        :class="show ? 'hidden' : ''"
      >
        <g id="surface1">
          <path
            style="stroke: none; fill-opacity: 1"
            d="M 21 3 C 11.601563 3 4 10.601563 4 20 C 4 29.398438 11.601563 37 21 37 C 24.355469 37 27.460938 36.015625 30.09375 34.34375 L 42.375 46.625 L 46.625 42.375 L 34.5 30.28125 C 36.679688 27.421875 38 23.878906 38 20 C 38 10.601563 30.398438 3 21 3 Z M 21 7 C 28.199219 7 34 12.800781 34 20 C 34 27.199219 28.199219 33 21 33 C 13.800781 33 8 27.199219 8 20 C 8 12.800781 13.800781 7 21 7 Z "
          />
        </g>
      </svg>
    </button>
    <button @click="hideSearch"  :class="show ? '' : 'hidden'">
      <img :src="require('@/assets/icons/Delete.svg')" class="w-6 mr-3 lg:ml-2">
    </button>

  </div>
</template>

<script>

export default {
  data(){
    return{
      show:false,
    }
  },

  methods:{
    showSearch() {
      this.show = true;
    },
    hideSearch() {
      this.show = false;
    },

  }
};
</script>

<style>
</style>
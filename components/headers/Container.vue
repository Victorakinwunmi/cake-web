<template>
  <div class="flex justify-between w-full p-4 fixed items-center z-100" :class="sticky_nav ? 'bg-pink-100' : ''">
    <div>
      <slot name="logo" />
    </div>

    <div class="">
      <div
        :class="is_revealed ? 'hidden' : 'block lg:hidden'"
        @click="showMenu"
        class="p-4"
      >
        <div class="">
          <slot name="hamburgermenuopen"></slot>
        </div>
      </div>

      <div
        :class="is_revealed ? 'block' : 'hidden lg:hidden'"
        @click="hideMenu"
        class="p-4"
      >
        <div>
          <slot name="hamburgermenuclose"></slot>
        </div>
      </div>
    </div>

    <div
      :class="
        is_revealed
          ? 'block top-14 right-0 w-full h-screen absolute mt-11 bg-gradient-to-t from-pink-200 to-white '
          : 'hidden lg:flex '
      "
      class=""
    >
      <div class="">
        <slot name="menu" />
      </div>

      <div
        class="block mt-8 mx-6 lg:mx-0 lg:mt-0 lg:flex items-center lg:ml-28"
      >
        <div>
          <slot name="search" />
        </div>

        <div>
          <slot name="shop" />
        </div>

        <div>
          <slot name="button" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    scrollPoint: {
      default: 115,
      type: Number,
    },
  },
  data() {
    return {
      is_revealed: false,
      sticky_nav: false,
    };
  },
  methods: {
    showMenu() {
      this.is_revealed = true;
    },
    hideMenu() {
      this.is_revealed = false;
    },

    handleStickyNavigation() {
      if (window.pageYOffset > this.scrollPoint) {
        this.sticky_nav = true;
      } else {
        this.sticky_nav = false;
      }
    },
  },

  beforeMount() {
    window.addEventListener("scroll", this.handleStickyNavigation);
  },

  beforeDestroy() {
    window.removeEventListener("scroll", this.handleStickyNavigation);
  },
};
</script>

<style>
</style>
<template>
  <div
    class="
      flex
      justify-between
      bg-pink-300
      w-full
      p-4
      shadow-xl
      fixed
      items-center
    "
  >
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
      :class="is_revealed ? 'block top-14 right-0 w-full h-screen mt-11 absolute bg-pink-300 ' : 'hidden lg:flex'"
      class="flex"
    >
      <div>
        <slot name="menu" />
      </div>

    </div>
    <div class="hidden lg:flex items-center">
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
</template>

<script>
export default {
  data() {
    return {
      is_revealed: false,
    };
  },
  methods: {
    showMenu() {
      this.is_revealed = true;
    },
    hideMenu() {
      this.is_revealed = false;
    },
  },
};
</script>

<style>
</style>
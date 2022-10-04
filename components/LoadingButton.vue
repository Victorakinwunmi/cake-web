<template>
  <div>
    <button
      :class="
        color ? color : 'hover:bg-gray-400 text-black'
      "
      @click="toggleLoad"
      :disabled="loading || disabled"
      class="
        font-bold
        rounded-md
        focus:text-gray-600 focus:outline-none
        outline-none
        my-10
        py-4
        px-10
        bg-gray-300
      "
    >
      <div class="flex items-center justify-center uppercase">
        <div v-if="loading" class="flex items-center">
          {{ loadingText }}
        </div>
        <div v-if="!loading">
          <slot name="login" />
        </div>
      </div>
    </button>
  </div>
</template>

<script>
export default {
  name: "LoadingButton",
  props: {
    loading: Boolean,
    color: String,
    disabled: Boolean,
    loadingText: String,
  },
  data() {
    return {
      loading_state: false,
    };
  },

  methods: {
    toggleLoad() {
      this.$emit("toggleLoad");
    },
  },
};
</script>

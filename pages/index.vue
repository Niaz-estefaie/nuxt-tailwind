<template>
  <div class="relative flex items-top justify-center min-h-screen sm:items-center sm:pt-0">
    <button
      class="btn border border-gray-800 px-4 py-2 dark:border-gray-100 capitalize"
      @click="changeMode"
    >
      {{ btnLabel }}
    </button>
  </div>
</template>

<script>
export default {
  computed: {
    btnLabel() {
      return this.$colorMode.preference === "light" ? "dark" : "light";
    }
  },
  methods: {
    changeMode() {
      this.$colorMode.preference =
        this.$colorMode.preference === "light" ? "dark" : "light";
    }
  }
};
</script>
<style>
  @import '@/assets/styles/tailwind.css';
</style>

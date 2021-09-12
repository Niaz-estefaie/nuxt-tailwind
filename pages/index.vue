<template>
  <div class="relative flex items-top justify-center min-h-screen bg-green sm:items-center sm:pt-0">
    <button class="btn border border-white capitalize" @click="changeMode">
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
  @import '@/assets/styles/tailwind.css'
</style>

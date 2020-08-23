<template>
  <div id="app" class="md:w-2/3 px-4 md:px-0 mx-auto max-w-6xl">
    <BaseNavbar></BaseNavbar>
    <BaseMembers></BaseMembers>
    <BaseFooter></BaseFooter>
  </div>
</template>

<script>
import BaseMembers from "@/components/base/BaseMembers.vue";
import BaseNavbar from "@/components/base/BaseNavbar.vue";
import BaseFooter from "@/components/base/BaseFooter.vue";

export default {
  name: "App",
  components: {
    BaseMembers,
    BaseNavbar,
    BaseFooter,
  },
};
</script>

<style>
:root {
  --global-font-family: "Poppins", "Helvetica Neue", -apple-system,
    BlinkMacSystemFont, "Segoe UI", Roboto, Arial, sans-serif;
  --global-secundary-font-family: "PT Serif", "Helvetica Neue", -apple-system,
    BlinkMacSystemFont, "Segoe UI", Roboto, Arial, sans-serif;
  --global-footer-font-family: "Montserrat", "Helvetica Neue", -apple-system,
    BlinkMacSystemFont, "Segoe UI", Roboto, Arial, sans-serif;
  --global-font-size: 1rem;

  --font-weight-regular: 400;
  --font-weight-bold: 700;
}

html,
body {
  font-family: var(--global-font-family);
  font-size: 16px;
  font-weight: var(--font-weight-regular);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  scroll-behavior: smooth;
  max-width: 1920px;
  margin: 0 auto;
}
</style>

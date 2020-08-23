<template>
  <div id="app" class="w-2/3 mx-auto max-w-6xl">
    <NavbarComponent></NavbarComponent>
    <div class="grid grid-cols-3 grid-rows-2 gap-4">
      <MemberComponent
        v-for="(member, index) in members"
        :key="index"
        :member="member"
      ></MemberComponent>
    </div>
    <FooterComponent></FooterComponent>
  </div>
</template>

<script>
import MemberComponent from "@/components/MemberComponent.vue";
import NavbarComponent from "@/components/NavbarComponent.vue";
import FooterComponent from "@/components/FooterComponent.vue";

export default {
  name: "App",
  components: {
    MemberComponent,
    NavbarComponent,
    FooterComponent,
  },
  data: function() {
    return {
      members: [
        {
          name: "Bill Mahoney",
          role: "Product Owner",
          img: "/img/member1.png",
        },
        {
          name: "Soba Cabrera",
          role: "Art Director",
          img: "/img/member2.png",
        },
        {
          name: "Shae Le",
          role: "Tech Lead",
          img: "/img/member3.png",
        },
        {
          name: "Skylah Lu",
          role: "UX Designer",
          img: "/img/member4.png",
        },
        {
          name: "Griff Richards",
          role: "Developer",
          img: "/img/member5.png",
        },
        {
          name: "Stan John",
          role: "Developer",
          img: "/img/member6.png",
        },
      ],
    };
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

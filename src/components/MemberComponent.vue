<template>
  <div :class="['relative', `${margin}-16`]">
    <img
      class="w-5/6 md:w-5/6 xl:w-9/10 mb-4 "
      alt="Vue logo"
      :src="member.img"
    />
    <span
      class="absolute top-0 left-100 transform origin-top-left rotate-90 whitespace-no-wrap uppercase text-sm"
      >{{ member.role }}</span
    >
    <span class="font-bold">{{ member.name }}</span>
  </div>
</template>

<script>
export default {
  props: {
    member: Object,
  },
  data: function() {
    return {
      margin: "",
    };
  },
  methods: {
    setMargin() {
      this.margin =
        window.innerWidth <= 762
          ? this.member.marginMobile
          : this.member.marginDesktop;
    },
  },
  created() {
    window.addEventListener("resize", this.setMargin);
  },
  destroyed() {
    window.removeEventListener("resize", this.setMargin);
  },
  mounted() {
    this.setMargin();
  },
};
</script>

<style scoped></style>

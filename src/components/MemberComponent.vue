<template>
  <div :class="['relative', `${member.margin}-16`]">
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
};
</script>

<style scoped></style>

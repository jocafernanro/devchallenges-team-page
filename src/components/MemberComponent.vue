<template>
  <div class="relative">
    <img class="w-84" alt="Vue logo" :src="member.img" />
    <span
      class="caption absolute right-0 top-25 origin-top-right transform rotate-90 whitespace-no-wrap uppercase"
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
// inline-block align-top -ml-20 origin-top-right transform rotate-90 uppercase
</script>

<style scoped>
.caption {
  /* top: 25%; */
}
</style>

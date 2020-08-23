<template>
  <div class="relative">
    <img class="w-9/10" alt="Vue logo" :src="member.img" />
    <span
      class="caption absolute top-0 right-0 -mr-20 origin-top-left transform rotate-90"
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

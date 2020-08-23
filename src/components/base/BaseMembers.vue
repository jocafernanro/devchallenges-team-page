<template>
  <div
    class="grid md:grid-cols-3 grid-cols-2 grid-rows-2 md:gap-10 lg:gap-16 gap-8"
  >
    <MemberComponent
      v-for="(member, index) of members"
      :key="index"
      :member="member"
    ></MemberComponent>
  </div>
</template>

<script>
import MemberComponent from "@/components/MemberComponent.vue";

export default {
  components: {
    MemberComponent,
  },
  data: function() {
    return {
      members: [
        {
          name: "Bill Mahoney",
          role: "Product Owner",
          img: "/img/member1.png",
          margin: "mb",
        },
        {
          name: "Soba Cabrera",
          role: "Art Director",
          img: "/img/member2.png",
          margin: "mt",
        },
        {
          name: "Shae Le",
          role: "Tech Lead",
          img: "/img/member3.png",
          margin: "mb",
        },
        {
          name: "Skylah Lu",
          role: "UX Designer",
          img: "/img/member4.png",
          margin: "mb",
        },
        {
          name: "Griff Richards",
          role: "Developer",
          img: "/img/member5.png",
          margin: "mt",
        },
        {
          name: "Stan John",
          role: "Developer",
          img: "/img/member6.png",
          margin: "mb",
        },
      ],
    };
  },
};
</script>

<style></style>

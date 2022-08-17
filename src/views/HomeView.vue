<template>
  <div class="home">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <div class="bg-red-200">
      <button class="btn">home button</button>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "HomeView",
  components: {
    // HelloWorld,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/main";
.btn {
  background-color: $color;
}
</style>

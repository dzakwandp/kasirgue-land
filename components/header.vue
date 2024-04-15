<template>
  <div>
    <!-- header -->
    <div class="flex h-16 w-full bg-white shadow-md">
      <div class="flex w-1/3 items-center">
        <img :src="logo" class="w-24 mx-auto" @click="this.$route.push('/')"></img>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from "@/assets/images/logo.png"
export default {
  data() {
    return {
      logo: Logo
    }
  },
};
</script>

<style lang="scss" scoped></style>

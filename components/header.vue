<template>
  <div>
    <!-- header -->
    <div
      @scroll="handleScroll()"
      class="flex h-max w-full fixed py-4 transition ease-in-out duration-700 z-10"
      :class="isScrolled ? 'bg-white text-primary shadow-md' : 'text-white'">
      <div class="flex w-1/3 items-center">
        <NuxtLink
          to="/"
          class="w-28 mx-auto transition ease-in-out duration-700 cursor-pointer"
          @click="toTop()">
          <img :src="isScrolled ? logo : logoWhite" />
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>
import { Button } from "@/components/ui/button";
import LogoWhite from "@/assets/images/logo_white.png";
import Logo from "@/assets/images/logo.png";
export default {
  components: {
    Button,
  },
  data() {
    return {
      logoWhite: LogoWhite,
      logo: Logo,
      links: [
        { route: "/layanan", title: "Layanan" },
        { route: "/tentang", title: "Tentang" },
        { route: "/harga", title: "Harga" },
      ],
      isScrolled: false,
    };
  },
  methods: {
    handleScroll(event) {
      if (window.scrollY > 145) {
        this.isScrolled = true;
      }
      if (window.scrollY < 145) {
        this.isScrolled = false;
      }
    },
    toTop() {
      window.scrollTo({
        top: 0,
        behavior: "smooth",
      });
    },
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },
};
</script>

<style lang="scss" scoped></style>

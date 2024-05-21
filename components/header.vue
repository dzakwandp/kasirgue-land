<template>
  <div>
    <!-- header -->
    <div
      class="flex h-max w-full fixed py-4"
      :class="{ 'bg-white': isScrolled }"
    >
      <div class="flex w-1/3 items-center">
        <img :src="logo" class="w-32 mx-auto" @click="this.$route.push('/')" />
      </div>
      <div
        class="flex w-1/3 items-center justify-center gap-6 text-white font-medium"
      >
        <div v-for="items in links" :key="items.id" class="hover:underline">
          <NuxtLink :to="items.route">{{ items.title }}</NuxtLink>
        </div>
      </div>
      <div class="flex w-1/3 items-center justify-center">
        <a
          href="http://api.whatsapp.com/send?phone=6285888080045&text=Hallo%20kak,%20mau%20informasi%20selanjutnya%20tentang%20Kasirgue%20dong"
          target="_blank"
        >
          <Button class="text-white size-max gap-2"
            ><Whatsapp class="w-6 fill-white" />Chat Now</Button
          >
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import { Button } from "@/components/ui/button";
import Logo from "@/assets/images/logo_white.png";
import Whatsapp from "@/components/icons/whatsapp.vue";
export default {
  components: {
    Button,
    Whatsapp,
  },
  data() {
    return {
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
      console.log(event);
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

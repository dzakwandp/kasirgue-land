<template>
  <div>
    <!-- header -->
    <div class="flex h-16 w-full fixed">
      <div class="flex w-1/3 items-center">
        <img :src="logo" class="w-24 mx-auto" @click="this.$route.push('/')" />
      </div>
      <div
        class="flex w-1/3 items-center justify-center gap-6 text-white font-medium"
      >
        <div v-for="items in links" :key="items.id" class="hover:underline">
          <NuxtLink :to="items.route">{{ items.title }}</NuxtLink>
        </div>
      </div>
      <div class="flex w-1/3 items-center justify-center">
        <a href="http://api.whatsapp.com/send?phone=6285888080045&text=Hallo%20kak,%20mau%20informasi%20selanjutnya%20tentang%20Kasirgue%20dong" target="_blank">
          <Button class="text-white">chat now</Button>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import { Button } from "@/components/ui/button";
import Logo from "@/assets/images/logo_white.png";
export default {
  components: {
    Button,
  },
  data() {
    return {
      logo: Logo,
      links: [
        { route: "/layanan", title: "Layanan" },
        { route: "/tentang", title: "Tentang" },
        { route: "/harga", title: "Harga" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>

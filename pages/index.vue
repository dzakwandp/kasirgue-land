<template>
  <div>
    <!-- first section -->
    <div
      class="flex w-full h-screen"
      :style="{ backgroundImage: `url(${bgImage})` }"
      style="
        background-size: cover;
        background-position: center center;
        opacity: 1;
        transform: none;
      "
    >
      <!-- left side -->
      <div
        class="flex flex-col h-full w-1/2 items-center justify-center gap-3 text-white"
      >
        <div class="text-6xl font-semibold">#SaatnyaOnline</div>
        <div class="text-2xl">
          Onlinekan Rekap Keuanganmu Sekarang dengan Kasirgue!
        </div>
        <div class="mx-6 text-xl text-justify">
          Dapatkan kemudahan dalam mengakses rekap keuanganmu dimanapun dan
          kapanpun dengan keamanan data terbaik bersama Kasirgue. Mulai buat
          sistem aplikasimu hanya dengan 150.000 per bulan.
        </div>
      </div>
      <!-- right side -->
      <div class="flex w-1/2 items-end justify-end">
        <img class="w-[80%] h-auto mr-4" :src="homeImage" alt="" />
      </div>
    </div>
    <!-- second section -->
    <div class="flex flex-col h-max w-full items-center mt-10 gap-4">
      <div class="text-primary font-semibold text-3xl">
        Apakah anda memiliki masalah seperti?
      </div>
      <div class="flex w-4/5 gap-6">
        <Card class="w-1/3" v-for="items in problems" :key="items.index">
          <img class="rounded-t-xl contrast-125" :src="items.image">
          <CardHeader>
            <CardTitle>{{ items.text }}</CardTitle>
          </CardHeader>
        </Card>
      </div>
    </div>
  </div>
</template>

<script>
import bgImage from "@/assets/images/first-bg.jpg";
import homeImage from "@/assets/images/home_picture.png";
import secondOneImage from "@/assets/images/2nd1.jpg"
import secondTwoImage from "@/assets/images/2nd2.jpg"
import secondThreeImage from "@/assets/images/2nd3.jpg"
import {
  Card,
  CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle,
} from "@/components/ui/card";
export default {
  components: {
    Card,
    CardContent,
    CardDescription,
    CardFooter,
    CardHeader,
    CardTitle,
  },
  data() {
    return {
      bgImage: bgImage,
      homeImage: homeImage,
      problems: [
        { image: secondOneImage, text: "Pencatatan masih dilakukan secara manual" },
        { image: secondTwoImage, text: "Pencatatan stok tidak efisien" },
        { image: secondThreeImage, text: "Kerugian disebabkan salah perhitungan" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>

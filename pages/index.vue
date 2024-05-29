<template>
  <div class="bg-[#e2e8f0]">
    <!-- first section -->
    <div
      class="flex w-full h-screen"
      :style="{ backgroundImage: `url(${bgImage})` }"
      style="
        background-size: cover;
        background-position: center center;
        opacity: 1;
        transform: none;
      ">
      <!-- left side -->
      <div
        class="flex flex-col h-full w-1/2 items-center justify-center gap-3 text-white">
        <div class="text-6xl font-semibold">#WaktunyaOnline</div>
        <div class="text-2xl">
          Online-in rekap keuangan Loe sekarang dengan Kasirgue!
        </div>
        <div class="mx-6 text-xl text-justify">
          Dapetin mudahnya mengakses rekap keuangan Loe dimanapun dan kapanpun
          dengan keamanan data terbaik bersama Kasirgue. Mulai buat sistem
          aplikasi Loe cuma dengan Rp<span class="font-number font-light"
            >150.000</span
          >
          per bulan.
        </div>
      </div>
      <!-- right side -->
      <div class="flex w-1/2 items-end justify-end">
        <img class="w-[80%] h-auto mr-4" :src="homeImage" alt="" />
      </div>
    </div>
    <!-- second section -->
    <div
      class="flex flex-col h-max w-full items-center mt-10 gap-4"
      data-aos="fade-up">
      <div class="text-primary font-semibold text-3xl">
        Kasirgue ada buat Loe
      </div>
      <div class="text-center font-semibold text-lg">
        Dengan Rp<span class="font-number font-normal">5000</span> per hari Loe
        sudah bisa dapetin aplikasi kasir yang bisa diakses 24 Jam.
      </div>
      <div class="flex gap-8">
        <Card class="flex w-1/2 flex-col gap-2 px-4 items-center shadow-none">
          <div
            class="flex w-2/3 bg-primary text-white text-xl p-2 rounded-b-sm justify-center">
            Basic
          </div>
          <CardContent class="font-number"> Rp150.000/bulan </CardContent>
        </Card>
        <Card class="flex w-1/2 flex-col gap-2 items-center shadow-none">
          <div
            class="flex w-2/3 bg-secondary text-white text-xl p-2 rounded-b-sm justify-center">
            Premium
          </div>
          <CardContent class="font-number"> Hubungi gue aja yok </CardContent>
        </Card>
      </div>
    </div>
    <!-- third section -->
    <div
      class="flex flex-col h-max w-full items-center mt-16 gap-4"
      data-aos="fade-up">
      <div class="text-primary font-semibold text-3xl">
        Kasirgue cocok untuk apapun bidang usaha Loe
      </div>
      <div class="flex flex-wrap justify-center w-5/6 gap-6">
        <Card
          class="w-1/6 hover:-translate-y-1 hover:scale-110 transition-all ease-in-out duration-300"
          v-for="items in usaha"
          :key="items.index">
          <img class="rounded-xl" :src="items.image" />
        </Card>
      </div>
    </div>
    <!-- fourth section -->
    <div
      class="flex flex-col h-max w-full items-center mt-16 gap-4"
      data-aos="fade-up">
      <div class="text-primary font-semibold text-3xl">
        Basic sama Premium? Bedanya apa sih?
      </div>
      <div class="text-center font-semibold text-lg">
        Bedanya? Dengan fitur premium Loe bisa request fitur yang pastinya akan
        sangat membantu usaha Loe.<br>
        Perbedaan lebih detail bisa Loe liat di tabel berikut yaa.
      </div>
    </div>
  </div>
</template>

<script>
import bgImage from "@/assets/images/first-bg.jpg";
import homeImage from "@/assets/images/home_picture.png";
import Kuliner from "@/assets/images/kuliner.jpg";
import OnlineShop from "@/assets/images/onlineshop.jpg";
import Rental from "@/assets/images/rental.jpg";
import Reparasi from "@/assets/images/reparasi.jpg";
import Kelontong from "@/assets/images/kelontong.jpg";
import Bangunan from "@/assets/images/bangunan.jpg";
import Fashion from "@/assets/images/fashion.jpg";
import Barbershop from "@/assets/images/barbershop.jpg";
import Laundry from "@/assets/images/laundry.jpg";
import Dsb from "@/assets/images/dsb.jpg";
import {
  Card,
  CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle,
} from "@/components/ui/card";
import {Table, TableBody, TableHeader, TableHead, TableRow,TableCell} from "@/components/ui/table"
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
      usaha: [
        { title: "Kuliner (FnB)", image: Kuliner },
        { title: "Online Shop", image: OnlineShop },
        { title: "Rental", image: Rental },
        { title: "Reparasi", image: Reparasi },
        { title: "Kelontong", image: Kelontong },
        { title: "Bangunan", image: Bangunan },
        { title: "Fashion", image: Fashion },
        { title: "Barbershop", image: Barbershop },
        { title: "Laundry", image: Laundry },
        { title: "Dsb", image: Dsb },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>

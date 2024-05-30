<template>
  <div class="bg-[#e2e8f0]">
    <!-- first section -->
    <div
      class="flex md:flex-row flex-col w-full h-screen"
      :style="{ backgroundImage: `url(${bgImage})` }"
      style="
        background-size: cover;
        background-position: center center;
        opacity: 1;
        transform: none;
      ">
      <!-- left side -->
      <div
        class="flex flex-col h-full md:w-1/2 w-full items-center justify-center gap-3 text-white">
        <div class="md:text-6xl text-5xl font-semibold">#WaktunyaOnline</div>
        <div class="text-2xl md-mx-0 mx-6 text-center">
          Online-in rekap keuangan Loe sekarang dengan Kasirgue!
        </div>
        <div class="mx-6 md:text-xl text-lg text-justify md:ml-10">
          Dapetin mudahnya mengakses rekap keuangan Loe dimanapun dan kapanpun
          dengan keamanan data terbaik bersama Kasirgue. Mulai buat sistem
          aplikasi Loe cuma dengan Rp<span class="font-number font-light"
            >150.000</span
          >
          per bulan.
        </div>
      </div>
      <!-- right side -->
      <div class="flex md:w-1/2 w-full items-end justify-end">
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
      <div
        class="flex md:flex-row flex-col gap-8 w-full justify-center md:items-stretch items-center">
        <Card
          class="flex md:w-1/5 w-1/2 flex-col gap-2 px-4 items-center shadow-none">
          <div
            class="flex w-2/3 bg-primary text-white text-xl p-2 rounded-b-sm justify-center">
            Basic
          </div>
          <CardContent class="text-xl text-primary font-bold font-number">
            Rp150.000/bulan
          </CardContent>
        </Card>
        <Card
          class="flex md:w-1/5 w-1/2 flex-col gap-2 items-center shadow-none">
          <div
            class="flex w-2/3 bg-secondary text-white text-xl p-2 rounded-b-sm justify-center">
            Premium
          </div>
          <CardContent class="flex flex-col items-center font-number gap-4">
            <div class="md:text-normal text-sm">Hubungi gue aja yok</div>
            <a
              href="http://api.whatsapp.com/send?phone=6285888080045&text=Hallo%20kak,%20mau%20informasi%20selanjutnya%20tentang%20Kasirgue%20dong"
              target="_blank">
              <Button class="text-white size-max gap-2">
                <Whatsapp class="w-6 fill-white" />Chat Gue
              </Button>
            </a>
          </CardContent>
        </Card>
      </div>
    </div>
    <!-- third section -->
    <div
      class="flex flex-col h-max w-full items-center mt-16 gap-4"
      data-aos="fade-up">
      <div class="text-primary font-semibold text-3xl text-center">
        Kasirgue cocok untuk apapun bidang usaha Loe
      </div>
      <div class="flex flex-wrap justify-center w-5/6 gap-6">
        <Card
          class="md:w-1/6 w-1/3 hover:-translate-y-1 hover:scale-110 transition-all ease-in-out duration-300"
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
      <div class="text-primary font-semibold text-3xl text-center">
        Basic sama Premium? Bedanya apa sih?
      </div>
      <div class="text-center font-semibold text-lg md:mx-0 mx-2">
        Bedanya? Dengan fitur premium Loe bisa request fitur yang pastinya akan
        sangat membantu usaha Loe.<br />
        Perbedaan lebih detail bisa Loe liat di tabel berikut yaa.
      </div>
      <Table class="md:w-1/3 w-2/3 mx-auto text-lg">
        <TableHeader>
          <TableRow>
            <TableHead class="font-bold text-primary text-center">
              Basic
            </TableHead>
            <TableHead class="font-bold text-secondary text-center">
              Premium
            </TableHead>
          </TableRow>
        </TableHeader>
        <TableBody>
          <TableRow v-for="items in content" :key="items.index">
            <TableCell>{{ items.basic }}</TableCell>
            <TableCell>{{ items.premium }}</TableCell>
          </TableRow>
        </TableBody>
      </Table>
    </div>
    <!-- fifth section -->
    <div
      class="flex flex-col w-full h-max py-8 bg-primary items-center mt-8"
      data-aos="fade-up">
      <div class="text-white font-semibold text-3xl text-center">
        Daripada bingung, yok segera hubungi Gue!
      </div>
      <div class="text-white font-semibold text-lg text-center">
        Dengan fitur-fitur diatas, tentunya Kasirgue akan berikan harga yang
        menarik buat Loe-Loe yang ingin mengembangkan usaha!
      </div>
      <div class="flex w-full mt-10">
        <div class="flex flex-col md:w-1/2">
          <div class="flex md:flex-row flex-col justify-center md:items-stretch items-center gap-4 h-max">
            <Card
              class="flex md:w-1/3 w-2/3 flex-col gap-2 px-4 items-center shadow-none">
              <div
                class="flex w-2/3 bg-primary text-white text-xl p-2 rounded-b-sm justify-center">
                Basic
              </div>
              <CardContent class="font-number text-center">
                <div class="text-2xl text-primary font-bold">Rp5.000/hari</div>
                <div>Rp150.000/bulan</div>
                <div class="line-through mt-4 text-black/60">
                  Rp1.800.000/tahun
                </div>
                <div class="text-xl text-primary font-bold">
                  Rp1.500.000/tahun
                </div>
                <div class="italic text-xs">
                  *khusus langganan langsung selama satu tahun
                </div>
              </CardContent>
            </Card>
            <Card class="flex md:w-1/3 w-2/3 flex-col gap-2 items-center shadow-none">
              <div
                class="flex w-2/3 bg-secondary text-white text-xl p-2 rounded-b-sm justify-center">
                Premium
              </div>
              <CardContent
                class="flex flex-col items-center text-center font-number">
                Hubungi gue untuk tentuin fitur yang Loe butuhin
                <a
                  href="http://api.whatsapp.com/send?phone=6285888080045&text=Hallo%20kak,%20mau%20informasi%20selanjutnya%20tentang%20Kasirgue%20dong"
                  target="_blank">
                  <Button class="text-white size-max gap-2">
                    <Whatsapp class="w-6 fill-white" />Chat Gue
                  </Button>
                </a>
              </CardContent>
            </Card>
          </div>
          <div class="text-white text-center mt-4">
            *Harga diatas sudah termasuk free akses 45 hari pertama.
          </div>
          <div class="text-white text-center md:text-5xl text-4xl font-semibold">
            #WaktunyaOnline
          </div>
        </div>
        <div class="hidden md:flex w-1/2 justify-center">
          <img :src="MascotDrink" class="w-1/5" />
        </div>
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
import MascotDrink from "@/assets/images/mascotdrink.png";
import Whatsapp from "@/components/icons/whatsapp.vue";
import {
  Card,
  CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle,
} from "@/components/ui/card";
import {
  Table,
  TableBody,
  TableHeader,
  TableHead,
  TableRow,
  TableCell,
} from "@/components/ui/table";
export default {
  components: {
    Card,
    CardContent,
    CardDescription,
    CardFooter,
    CardHeader,
    CardTitle,
    Table,
    TableBody,
    TableHeader,
    TableHead,
    TableRow,
    TableCell,
    Whatsapp,
  },
  data() {
    return {
      bgImage: bgImage,
      homeImage: homeImage,
      MascotDrink: MascotDrink,
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
      content: [
        { basic: "Ringkasan Bisnis", premium: "Pengelolaan Supplier" },
        { basic: "Pengelolaan Produk", premium: "Pengelolaan Pelanggan" },
        {
          basic: "Pengelolaan Penjualan",
          premium: "Sistem Barcode dan Labeling",
        },
        { basic: "Pengelolaan Stok", premium: "Foto Produk" },
        {
          basic: "Pengelolaan Pembelian",
          premium: "Dan lainnya sesuai custom Loe",
        },
        { basic: "Laporan Laba Rugi", premium: "" },
        { basic: "Sistem Berbasis Online", premium: "" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>

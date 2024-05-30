<template>
  <div class="flex flex-col w-full h-max bg-secondary">
    <!-- separator -->
    <div class="w-full bg-[#e2e8f0] h-[10px]"></div>
    <div class="flex md:flex-row flex-col w-full h-max md:px-40 md:py-20 md:mt-0 mt-4 items-center">
      <div class="flex md:w-1/3 w-full">
        <img :src="LogoWhite" class="size-1/3 md:mx-0 mx-auto" />
      </div>
      <div class="flex md:w-2/3 md:gap-0 gap-2">
        <div class="flex w-1/2 flex-col text-white">
          <div>Office:</div>
          <div class="md:text-normal text-sm">Perum Puri Margomulyo Asri No. 56, Seyegan, Sleman</div>
          <div>55561</div>
        </div>
        <div class="flex w-1/2 flex-col text-white">
          <div>Social:</div>
          <div class="flex gap-2">
            <a href="https://instagram.com/kasirgue" target="_blank">
              <Instagram class="fill-white size-8"></Instagram>
            </a>
            <a
              href="http://api.whatsapp.com/send?phone=6285888080045&text=Hallo%20kak,%20mau%20informasi%20selanjutnya%20tentang%20Kasirgue%20dong"
              target="_blank">
              <Whatsapp class="fill-white size-8"></Whatsapp>
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="flex mx-auto md:w-10/12 w-11/12 bg-[#e2e8f0] h-[2px]"></div>
    <div class="text-white text-center mt-2 font-number text-sm">Copyright ©2024 Kasirgue.com</div>
  </div>
</template>

<script>
import LogoWhite from "@/assets/images/logo_white.png";
import Instagram from "@/components/icons/instagram.vue";
import Whatsapp from "@/components/icons/whatsapp.vue";
export default {
  components: {
    Instagram,
    Whatsapp,
  },
  data() {
    return {
      LogoWhite: LogoWhite,
    };
  },
};
</script>

<style lang="scss" scoped></style>

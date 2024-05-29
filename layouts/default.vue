<template>
  <div>
    <Header />
    <slot />
    <!-- chat button -->
    <div class="flex fixed w-max right-0 bottom-0 mr-2 mb-2 z-10">
      <a
        href="http://api.whatsapp.com/send?phone=6285888080045&text=Hallo%20kak,%20mau%20informasi%20selanjutnya%20tentang%20Kasirgue%20dong"
        target="_blank">
        <Button class="text-white size-max gap-2"
          ><Whatsapp class="w-6 fill-white" />Chat Now</Button
        >
      </a>
    </div>
  </div>
</template>

<script>
import Whatsapp from "@/components/icons/whatsapp.vue";
import Header from "@/components/header.vue";
export default {
  components: {
    Header,
    Whatsapp
  },
};
</script>

<style lang="scss" scoped></style>

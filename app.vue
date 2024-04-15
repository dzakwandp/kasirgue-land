<template>
  <div class="min-h-screen min-w-full">
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</div>
</template>

<script>
export default {
  setup() {
    useSeoMeta({
      title: "Kasirgue",
    });
  },
};
</script>

<script setup>
const { t } = useI18n()
</script>

<template>
  <div class="hero-bg left-0 top-0">
    <h1 class="ml-[310px] mr-[310px] pt-[310px] text-center text-[4rem] font-600 leading-[96px] text-white">
      {{ t('intro.title') }}
    </h1>
    <h2 class="ml-[328px] mr-[328px] mt-[40px] pb-[452px] text-center text-[1.5rem] leading-[48px] text-white">
      {{ t('intro.desc') }}
    </h2>
  </div>

  <TheTravelFilter />
</template>

<style scoped>
.hero-bg {
    background-image: url('~/assets/pexels-francesco-ungaro-2835436 1.png');
    @apply bg-center bg-cover bg-no-repeat;

}
</style>

<script setup>
const tabs = ref([
  {
    id: 1,
    label: 'flight',
  },
  {
    id: 2,
    label: 'Hotel',
  },
  {
    id: 3,
    label: 'chuj',
  },
])
</script>

<template>
  <div class="absolute left-0 right-0 ml-[130px] mr-[130px] rounded-bl-[50px] rounded-br-[50px] rounded-tr-[50px] bg-white -bottom-90">
    <div class="mb-[60px] ml-[48px] mt-[60px] flex items-center">
      <AppTabs />
      <TheBoxCitiesSmall />
      <TheBoxDatesSmall />
      <button class="ml-[40px] rounded-[65px] bg-blue p-[3.125rem]">
        <img src="src/assets/Group 9.svg" alt="">
      </button>
    </div>
  </div>
</template>

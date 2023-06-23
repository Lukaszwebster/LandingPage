<script setup>
const props = defineProps({
  secondary: {
    type: Boolean,
    default: false,
  },
})
</script>

<template>
  <!-- ostylowany button. Jesli bedzie mial wartosc secondary przyjmie inne style -->
  <button
    type="button"
    class="ml-[50px] rounded-xl pb-[14px] pl-[44px] pr-[44px] pt-[14px] text-[1.5rem] text-blue hover:bg-teal-200"
    :class="props.secondary ? 'bg-[#F2F6FF]' : 'bg-white' "
  >
    <slot />
  </button>
</template>

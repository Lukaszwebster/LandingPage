<script setup>
const props = defineProps({
  secondary: {
    type: Boolean,
    default: false,
  },
})
</script>

<template>
  <button
    type="button"
    class="ml-[50px] rounded-xl bg-white pb-[14px] pl-[44px] pr-[44px] pt-[14px] text-[1.5rem] text-blue hover:bg-teal-200"
    :class="props.secondary ? 'bg-bluegray' : 'bg-cyan' "
  >
    <slot />
  </button>
</template>

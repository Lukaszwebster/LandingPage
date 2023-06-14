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
    class="rounded-3xl pb-2 pl-8 pr-8 pt-2 text-white hover:bg-teal-200"
    :class="props.secondary ? 'bg-bluegray' : 'bg-cyan' "
  >
    <slot />
  </button>
</template>

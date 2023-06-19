<script setup>
const props = defineProps ({
  tabs: {
    type: Array,
    default() {
      return []
    },
  },

})
</script>

<template>
  <div>
    <ul>
      <li v-for="item in props.tabs" :key="item.id">
        {{ item.id }} {{ item.label }}
      </li>
    </ul>
  </div>
</template>

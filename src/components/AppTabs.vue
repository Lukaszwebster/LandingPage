<script setup>
const props = defineProps ({
  tabs: {
    type: Array,
    default() {
      return []
    },
  },
  modelValue: {
    type: Number,
  },

})
const emit = defineEmits([
  'update:modelValue',
])
</script>

<template>
  <div class="relative">
    {{ props.modelValue }}
    <ul class="absolute flex gap-2 -top-10">
      <li
        v-for="item in props.tabs" :key="item.id" class="" :class="props.modelValue === item.id ? 'bg-blue' : 'bg-none'"
        @click="emit('update:modelValue', item.id)"
      >
        {{ item.id }} {{ item.label }}
      </li>
    </ul>
    <div v-for="item in props.tabs" v-show="props.modelValue === item.id" :key="item.id" class="tabContent">
      <slot :name="item.id" />
    </div>
  </div>
</template>

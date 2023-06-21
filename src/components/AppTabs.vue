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
    <!-- {{ props.modelValue }} -->
    <ul class="absolute h-[100px] flex gap-2 rounded-lt-[20px] rounded-rt-[20px] bg-white p-4 -top-38">
      <li
        v-for="item in props.tabs" :key="item.id" class="" :class="props.modelValue === item.id ? 'bg-lightBlueButton p-2 rounded-[10px] h-[40px] text-18px cursor-pointer' : 'cursor-pointer bg-none p-2 rounded-[10px] text-18px'"
        @click="emit('update:modelValue', item.id)"
      >
        {{ item.label }}
      </li>
    </ul>
    <div v-for="item in props.tabs" v-show="props.modelValue === item.id" :key="item.id" class="tabContent mb-[60px] ml[48px] mt-[60px] flex">
      <slot :name="item.id" />
    </div>
  </div>
</template>

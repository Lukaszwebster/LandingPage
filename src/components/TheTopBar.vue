<script setup>
const props = defineProps ({
  items: {
    type: Array,
    default() {
      return []
    },
  },

})
const { t } = useI18n()
</script>

<template>
  <div class="absolute left-0 right-0 ml-[8.125rem] mr-[8.125rem] mt-[1.5rem] flex justify-between">
    <div class="text-[3rem] text-white">
      Treloo
    </div>
    <div class="flex items-center">
      <nav>
        <ul class="flex gap-[50px] text-[1.5rem] text-white">
          <li v-for="item in props.items" :key="item.id">
            {{ item.label }}
          </li>
        </ul>
      </nav>
      <AppButton>
        {{ t('button.blog') }}
      </AppButton>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { useLayoutStore } from '@/stores/modules/layout';

defineOptions({ name: 'app-trigger' });

const $layoutStore = useLayoutStore();

const toggle = () => {
  $layoutStore.drawer = !$layoutStore.drawer;
  window.dispatchEvent(new Event('resize'));
};
</script>

<template>
  <div @click="toggle" class="absolute top-1/2 left-0 -translate-y-1/2 h-20 w-4 flex flex-col justify-center items-center cursor-pointer group">
    <template v-if="$layoutStore.drawer">
      <div class="h-3 w-1 rounded-full bg-gray-500 translate-y-0.5 duration-300 group-hover:rotate-12"></div>
      <div class="h-3 w-1 rounded-full bg-gray-500 -translate-y-0.5 duration-300 group-hover:-rotate-12"></div>
    </template>
    <template v-else>
      <div class="h-3 w-1 rounded-full bg-gray-500 translate-y-0.5 duration-300 group-hover:-rotate-12"></div>
      <div class="h-3 w-1 rounded-full bg-gray-500 -translate-y-0.5 duration-300 group-hover:rotate-12"></div>
    </template>
  </div>
</template>

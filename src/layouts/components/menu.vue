<script lang="ts" setup>
import { useLayoutStore } from '@/stores/modules/layout';
import menu from '@/assets/json/menu.json';

defineOptions({ name: 'app-menu' });

const $layoutStore = useLayoutStore();

console.log(menu);
</script>

<template>
  <q-drawer v-model="$layoutStore.drawer" :width="200" bordered>app-menu</q-drawer>
</template>

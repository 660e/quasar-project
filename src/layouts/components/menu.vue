<script lang="ts" setup>
import { useLayoutStore } from '@/stores/modules/layout';

defineOptions({ name: 'app-menu' });

const $layoutStore = useLayoutStore();
</script>

<template>
  <q-drawer v-model="$layoutStore.drawer" :width="200" bordered>app-menu</q-drawer>
</template>

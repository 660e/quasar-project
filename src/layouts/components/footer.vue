<script lang="ts" setup>
import $package from '../../../package.json';

defineOptions({ name: 'app-footer' });
</script>

<template>
  <q-footer>
    <q-separator />
    <div class="h-9 px-4 flex justify-between items-center">
      <div class="space-x-2 flex">
        <span>Home</span>
        <span>/</span>
        <span>Components</span>
        <span>/</span>
        <span>Breadcrumbs</span>
      </div>
      <div>{{ $package.version }}</div>
    </div>
  </q-footer>
</template>

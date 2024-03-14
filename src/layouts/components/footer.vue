<script lang="ts" setup>
import $package from '../../../package.json';

defineOptions({ name: 'app-footer' });
</script>

<template>
  <q-footer class="bg-transparent">
    <q-separator />
    <div :class="[$q.dark.isActive ? 'text-white' : 'text-dark']" class="h-9 px-4 flex justify-between items-center">
      <div class="flex space-x-2">
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

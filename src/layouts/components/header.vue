<script lang="ts" setup>
defineOptions({ name: 'app-header' });
</script>

<template>
  <q-header class="h-12 pl-4 pr-2 flex items-center">
    <div class="leading-none text-2xl">Quasar App</div>
    <q-space />
    <q-btn icon="mail" size="12px" flat round>
      <q-badge color="negative" floating>99</q-badge>
    </q-btn>
    <q-btn icon="g_translate" size="12px" flat round />
    <q-btn @click="$q.dark.toggle" size="12px" icon="compare" flat round />
    <q-btn size="12px" flat round>
      <q-avatar size="20px" rounded>
        <img src="https://avatars.githubusercontent.com/u/28943787" />
      </q-avatar>
    </q-btn>
  </q-header>
</template>

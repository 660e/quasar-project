<script lang="ts" setup>
defineOptions({ name: 'app-header' });
</script>

<template>
  <q-header class="h-12 pl-4 pr-2 flex items-center">
    <div class="leading-none text-2xl">Quasar App</div>
    <q-space />
    <q-btn size="12px" flat round>
      <q-icon name="travel_explore" size="20px" />
    </q-btn>
    <q-btn size="12px" flat round>
      <q-icon name="mail" size="20px" />
      <q-badge color="negative" floating>99</q-badge>
    </q-btn>
    <q-btn size="12px" flat round>
      <q-icon name="g_translate" size="20px" />
    </q-btn>
    <q-btn @click="$q.dark.toggle" size="12px" flat round>
      <q-icon name="compare" size="20px" />
    </q-btn>
    <q-btn size="12px" flat round>
      <q-avatar size="20px">
        <img src="https://avatars.githubusercontent.com/u/28943787" />
      </q-avatar>
    </q-btn>
  </q-header>
</template>

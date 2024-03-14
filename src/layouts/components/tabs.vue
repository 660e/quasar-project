<script lang="ts" setup>
import { ref } from 'vue';

defineOptions({ name: 'app-tabs' });

const tab = ref('mails');
</script>

<template>
  <q-tabs v-model="tab" align="left" dense>
    <q-tab name="mails" label="Mails" />
    <q-tab name="alarms" label="Alarms" />
    <q-tab name="movies" label="Movies" />
  </q-tabs>
  <q-separator />
</template>

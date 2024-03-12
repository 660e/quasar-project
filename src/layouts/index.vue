<script lang="ts" setup>
import AppHeader from './components/header.vue';
import AppFooter from './components/footer.vue';

defineOptions({ name: 'app-layout' });
</script>

<template>
  <q-layout view="hhh lpr lfr">
    <app-header />
    <app-footer />
  </q-layout>
</template>

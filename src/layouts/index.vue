<script lang="ts" setup>
import AppHeader from './components/header.vue';
import AppFooter from './components/footer.vue';
import AppMenu from './components/menu.vue';
import AppTabs from './components/tabs.vue';
import AppTrigger from './components/trigger.vue';

defineOptions({ name: 'app-layout' });

const tweak = (offset: number, height: number) => ({ height: `${height - offset - 36 - 1}px` });
</script>

<template>
  <q-layout view="hhh lpr lfr" class="overflow-hidden">
    <app-header />
    <app-footer />
    <app-menu />

    <q-page-container>
      <app-tabs />
      <q-page :style-fn="tweak" class="overflow-y-auto overflow-x-hidden relative">
        <app-trigger />
      </q-page>
    </q-page-container>
  </q-layout>
</template>

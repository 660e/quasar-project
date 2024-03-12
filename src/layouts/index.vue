<script lang="ts" setup>
import AppHeader from './components/header.vue';
import AppFooter from './components/footer.vue';
import AppMenu from './components/menu.vue';
import AppTabs from './components/tabs.vue';
import AppBreadcrumbs from './components/breadcrumbs.vue';

defineOptions({ name: 'app-layout' });
</script>

<template>
  <q-layout view="hhh lpr lfr">
    <app-header />
    <app-footer />
    <app-menu />

    <q-page-container>
      <q-page>
        <app-tabs />
        <app-breadcrumbs />
      </q-page>
    </q-page-container>
  </q-layout>
</template>

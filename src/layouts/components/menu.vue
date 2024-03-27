<script lang="ts" setup>
import { h, VNode } from 'vue';
import { QExpansionItem, QItem, QItemSection, QList } from 'quasar';
import { useLayoutStore } from '@/stores/modules/layout';
import menus from '@/assets/json/menus.json';

defineOptions({ name: 'app-menu' });

interface Menu {
  path: string;
  name: string;
  meta: {
    label: string;
  };
  component?: string;
  children?: Menu[];
}

const $layoutStore = useLayoutStore();

const menuList = () => h(QList, () => menus.map(menu => menuItem(menu)));
const menuItem = (menu: Menu): VNode => {
  if (menu.children?.length) {
    return h(QExpansionItem, { label: menu.meta.label }, () => menu.children?.map(m => menuItem(m)));
  } else {
    return h(QItem, { clickable: true }, () => h(QItemSection, () => menu.meta.label));
  }
};
</script>

<template>
  <q-drawer v-model="$layoutStore.drawer" :width="230" bordered>
    <menu-list />
  </q-drawer>
</template>

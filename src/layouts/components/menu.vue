<script lang="ts" setup>
import { useLayoutStore } from '@/stores/modules/layout';
import menus from '@/assets/json/menus.json';

defineOptions({ name: 'app-menu' });

const $layoutStore = useLayoutStore();

console.log(menus);
</script>

<template>
  <q-drawer v-model="$layoutStore.drawer" :width="220" bordered>
    <q-list>
      <template v-for="menu in menus" :key="menu.name">
        <q-expansion-item v-if="menu.children?.length" :label="menu.meta.label">
          <q-list>
            <q-item v-for="m in menu.children" :key="m.name" clickable v-ripple>
              <q-item-section>{{ m.meta.label }}</q-item-section>
            </q-item>
          </q-list>
        </q-expansion-item>
        <q-item v-else clickable v-ripple>
          <q-item-section>{{ menu.meta.label }}</q-item-section>
        </q-item>
      </template>
    </q-list>
  </q-drawer>
</template>

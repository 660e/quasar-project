<script lang="ts" setup>
import { reactive, ref } from 'vue';
import { useRouter } from 'vue-router';

defineOptions({ name: 'app-login' });

const form = reactive({
  username: 'admin',
  password: '123456'
});

const $router = useRouter();
const loading = ref(false);
const signIn = () => {
  loading.value = true;
  setTimeout(() => {
    loading.value = false;
    $router.push({ name: 'home' });
  }, 3000);
};
</script>

<template>
  <q-card class="h-screen flex justify-center" flat>
    <div class="flex flex-col items-center">
      <img src="@/assets/quasar-logo-vertical.svg" class="w-40" />
      <div class="w-80 border border-gray-300 bg-gray-100 rounded p-4 space-y-4">
        <q-input v-model="form.username" :disable="loading" label="Username" class="bg-white" outlined />
        <q-input v-model="form.password" :disable="loading" label="Password" class="bg-white" type="password" outlined />
        <q-btn :loading="loading" @click="signIn" label="Sign in" color="primary" class="w-full" no-caps unelevated />
      </div>
    </div>
  </q-card>
</template>

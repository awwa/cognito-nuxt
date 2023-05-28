<template>
  <div>
    <NuxtWelcome />
    <VBtn>Vuetify のボタン</VBtn>
  </div>
</template>

<script setup lang="ts">
import { Configuration, DefaultApi } from "@/api-client"
const config = new Configuration({ basePath: 'http://localhost:3100' });
const api = new DefaultApi(config);
const car = await api.carsControllerFindOne({ id: 'car_1' });
console.log(car.modelName);
</script>
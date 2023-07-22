<template>
  <Suspense>
    <template #default>
      <AsyncCityView />
    </template>
    <template #fallback>
      <CityViewSkeleton />
    </template>
  </Suspense>
</template>

<script setup>
import { useRoute } from "vue-router";
import AsyncCityView from "../components/AsyncCityView.vue";
import CityViewSkeleton from "../components/CityViewSkeleton.vue";

const route = useRoute();
</script>

<style scoped></style>

<script setup>
const route = useRoute();
const { capitalizeFirstLetter } = useUtilities();
useHead({
  title: `${
    route.params.make ? capitalizeFirstLetter(route.params.make) : "Cars"
  } in ${capitalizeFirstLetter(route.params.city)}`,
});
definePageMeta({
  layout: "custom",
});
</script>

<template>
  <!-- cars page -->
  <div class="flex mt-32">
    <CarSideBar />
    <NuxtPage />
  </div>
</template>

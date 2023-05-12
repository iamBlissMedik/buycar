<script setup>
const route = useRoute();
const { capitalizeFirstLetter } = useUtilities();
useHead({
  title: capitalizeFirstLetter(route.params.name),
});
definePageMeta({
  layout: "custom",
});
</script>

<template>
  <!-- car detail page -->

  <div>
    <CarDetailsHero />
    <CarDetailsAttributes />
    <CarDetailsDescription />
    <CarDetailsContact />
  </div>
</template>

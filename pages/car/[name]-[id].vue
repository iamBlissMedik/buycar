<script setup>
const route = useRoute();
const capitalizeFirstLetter = (string) => {
  return string.charAt(0).toUpperCase() + string.slice(1);
};
useHead({
  title: capitalizeFirstLetter(route.params.name),
});
</script>

<template>
  <!-- car detail page -->
  <div
    class="mx-auto mt-32 max-w-7xl space-y-4 px-4 xs:px-8 sm:px-10 lg:px-16 pb-16 w-3/5"
  >
    <CarDetailsHero />
    <CarDetailsAttributes />
    <CarDetailsDescription />
    <CarDetailsContact />
  </div>
</template>

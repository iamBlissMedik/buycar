<script setup>
const route = useRoute();
const capitalizeFirstLetter = (string) => {
  return string.charAt(0).toUpperCase() + string.slice(1);
};
useHead({
  title: `${
    route.params.make ? capitalizeFirstLetter(route.params.make) : "Cars"
  } in ${capitalizeFirstLetter(route.params.city)}`,
});
</script>

<template>
  <div
    class="mx-auto mt-4 max-w-7xl space-y-4 px-4 xs:px-8 sm:px-10 lg:px-16 pb-16 w-3/5"
  >
    <!-- cars page -->
    <div class="flex mt-32">
      <CarSideBar />
      <NuxtPage />
    </div>
  </div>
</template>

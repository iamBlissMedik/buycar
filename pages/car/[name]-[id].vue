<script setup>
const { cars } = useCars();
const route = useRoute();
const { capitalizeFirstLetter } = useUtilities();
useHead({
  title: capitalizeFirstLetter(route.params.name),
});
definePageMeta({
  layout: "custom",
});
const car = computed(() => {
  return cars.find((car) => car.id === parseInt(route.params.id));
});
if (!car.value) {
  throw createError({
    statusCode: 404,
    message: `Car with the id of ${route.params.id} does not exist`,
  });
}
</script>

<template>
  <!-- car detail page -->

  <div v-if="car">
    <CarDetailsHero :car="car" />
    <CarDetailsAttributes :attributes="car.features" />
    <CarDetailsDescription :description="car.description" />
    <CarDetailsContact />
  </div>
</template>

<script setup>
const { message, statusCode } = useError().value;

const handleError = () => {
  clearError({
    redirect: "/",
  });
};
</script>

<template>
  <div class="flex h-screen justify-center items-center flex-col">
    <h1 class="text-9xl">{{ statusCode }}</h1>
    <p class="mt-7 text-4xl">{{ message }}</p>
    <button
      class="rounded mt-7 bg-blue-400 px-7 py-4 text-white text-2xl"
      @click="handleError"
    >
      Go back
    </button>
  </div>
</template>

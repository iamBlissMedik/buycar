<script setup>
const props = defineProps({
  attributes: Array,
});
</script>
<template>
  <!-- car attributes -->
  <div class="mr-10 mt-5 border-b p-5">
    <div class="flex text-lg mt-2" v-for="(attribute,index) in attributes" :key="index">
      <p class="rounded text-lime-800 mr-3">√</p>
      <p>{{ attribute }}</p>
    </div>
  </div>
</template>

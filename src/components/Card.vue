<script setup>
import { defineProps } from "vue";

const props = defineProps({
  img: String,
  title: String,
  path: String,
});
</script>

<template>
  <router-link
    :to="{ name: 'detail', params: { id: props.path } }"
    class="flex justify-center items-center"
  >
    <div class="p-6 bg-white max-w-md shadow-md rounded-lg">
      <div class="flex flex-col gap-4">
        <img class="w-64" :src="props.img" :alt="props.title" />
        <h3 class="">{{ props.title }}</h3>
      </div>
    </div>
  </router-link>
</template>

<script lang="ts" setup></script>

<template>
  <div>
    <APanel>
      <h1 class="text-2xl">{{ label }}</h1>
      <img :src="src" alt="" class="rounded-md overflow-hidden my-2 aspect-square w-full object-cover">
      <slot/>
      <NuxtLink :to="dest">
        <ANavButton class="mt-2">Learn More</ANavButton>
      </NuxtLink>
    </APanel>
  </div>
</template>

<style scoped></style>

<script lang="ts">
export default {
  props: {
    label: {
      type: String,
      required: false,
    },
    src: {
      type: String,
      required: false,
    },
    dest: {
      type: String,
      required: false,
    }
  }
}
</script>
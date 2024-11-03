<script setup>
import { ref } from "vue";
const props = defineProps({
  initialCount: Number,
});
const counter = ref(props.initialCount ?? 0);
</script>

<template>
  <slot name="named"></slot>
  <button @click="($event) => counter++">{{ counter }}</button>
  <slot></slot>
</template>

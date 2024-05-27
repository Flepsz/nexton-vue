<script setup lang="ts">
import { ChevronRight } from "lucide-vue-next";

const props = defineProps<{
	class?: HTMLAttributes["class"];
}>();
</script>

<template>
	<ChevronRight :class="cn('size-4', props.class)" />
</template>

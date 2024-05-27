<script setup lang="ts">
import { Loader2 } from "lucide-vue-next";
import type { HTMLAttributes } from "vue";
import { cn } from "~~/lib/utils/";

const props = defineProps<{
	class?: HTMLAttributes["class"];
}>();
</script>

<template>
	<Loader2 :class="cn('size-4 mr-2 animate-spin', props.class)" />
</template>

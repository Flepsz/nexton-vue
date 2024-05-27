<script setup lang="ts">
defineProps<{
	first: string;
	second: string;
}>();
</script>

<template>
	<h1 class="text-foreground text-3xl font-semibold lg:text-4xl 2xl:text-5xl">
		{{ first }}
		<span class="text-foreground/70">{{ second }}</span>
	</h1>
</template>

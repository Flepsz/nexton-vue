<script setup lang="ts">
const props = defineProps<{
	title?: string;
	links?: string[];
}>();
</script>

<template>
	<div class="flex-1 flex flex-col gap-3 text-sm min-w-max">
		<h4 class="font-semibold text-base text-foreground">{{ props.title }}</h4>
		<div class="flex flex-col gap-3 font-normal">
			<a
				v-for="link in props.links"
				href="/"
				class="text-foreground/75 transition-colors hover:text-foreground/40"
				>{{ link }}</a
			>
		</div>
	</div>
</template>

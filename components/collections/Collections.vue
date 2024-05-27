<script setup lang="ts">
import { LucideArrowRight } from "lucide-vue-next";
function navigateShop(search: string) {
	navigateTo({
		path: "/shop",
		query: {
			search: search,
		},
	});
}

const collections = [
	{
		title: "For Men's",
		desc: "Starting at $24",
		href: "Roupa masculina",
	},
	{
		title: "For Women's",
		desc: "Starting at $19",
		href: "Roupa feminina",
	},
	{
		title: "Accessories",
		desc: "Explore accessories",
		href: "acessório",
	},
];
</script>

<template>
	<div class="flex gap-12 justify-between">
		<div
			v-for="item in collections"
			class="flex rounded-xl w-full justify-between px-7 py-10 bg-foreground/5"
		>
			<div class="pr-0 xl:pr-5">
				<h4 class="font-semibold text-lg text-foreground">{{ item.title }}</h4>
				<p class="text-foreground/70 text-sm">{{ item.desc }}</p>
			</div>
			<div
				class="flex gap-1 cursor-pointer items-center pl-2 transition-opacity hover:opacity-70"
			>
				<a
					@click="navigateShop(item.href)"
					class="text-xs text-foreground/70 uppercase"
					>Shop Now</a
				>
				<LucideArrowRight class="text-foreground/70 size-4" />
			</div>
		</div>
	</div>
</template>

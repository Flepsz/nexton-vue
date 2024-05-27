<script setup lang="ts">
import {
	Carousel,
	CarouselContent,
	CarouselItem,
	CarouselNext,
	CarouselPrevious,
} from "~/components/ui/carousel";
import { LucideSearch } from "lucide-vue-next";
import { Button } from "~/components/ui/button";

const props = defineProps<{
	search?: string;
}>();

const images: string[] = ["hero/hero.png", "hero/hero2.png", "hero/hero3.png"];

function goToShop() {
	navigateTo({
		path: "/shop",
		query: {
			search: props.search,
		},
	});
}
</script>

<template>
	<section class="flex items-center justify-center">
		<Carousel class="relative">
			<CarouselContent class="w-full ml-0">
				<CarouselItem class="pl-0 relative" v-for="img in images">
					<NuxtImg :src="img" class="flex items-center w-full justify-center" />
					<div class="absolute top-0 left-0 pl-20 h-full max-w-[50%]">
						<div class="flex flex-col gap-3 justify-center h-full lg:gap-5">
							<p class="text-zinc-700 text-sm lg:text-base">
								Starting from: $49.99
							</p>
							<h1
								class="text-indigo-950 font-semibold text-4xl lg:text-5xl 2xl:text-6xl"
							>
								Exclusive collection for everyone
							</h1>
							<Button
								@click="goToShop()"
								variant="outline"
								class="w-2/5 rounded-full bg-indigo-950 text-white font-light text-sm lg:text-base"
							>
								Explore now
								<LucideSearch class="ml-3 size-4" />
							</Button>
						</div>
					</div>
				</CarouselItem>
			</CarouselContent>
			<CarouselPrevious />
			<CarouselNext />
		</Carousel>
	</section>
</template>

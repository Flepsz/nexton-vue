<script setup lang="ts">
interface Footer {
	title: string;
	links: string[];
}
const footerLinks: Footer[] = [
	{
		title: "Getting started",
		links: ["Release Notes", "Upgrade Guide", "Browser Support", "Dark Mode"],
	},
	{
		title: "Explore",
		links: ["Prototyping", "Design systems", "Pricing", "Security"],
	},
	{
		title: "Community",
		links: [
			"Discussion Forums",
			"Code of Conduct",
			"Contributing",
			"API Reference",
		],
	},
];

const paymentIcons: string[] = [
	"pay-icons/visa.png",
	"pay-icons/paypal.png",
	"pay-icons/stripe.png",
	"pay-icons/verisign.png",
];
</script>

<template>
	<footer
		class="flex flex-col w-full gap-20 bg-light-white items-center justify-start lg:px-20 py-10 px-5 border-t border-foreground/10"
	>
		<div class="flex flex-col gap-12 w-full">
			<div class="flex flex-wrap justify-evenly">
				<app-logo />
				<footer-column
					v-for="links in footerLinks"
					:title="links.title"
					:links="links.links"
				/>
			</div>
		</div>
		<div
			class="flex justify-between border-t border-foreground/10 items-center max-sm:flex-col w-full text-sm font-normal pt-5"
		>
			<p class="text-foreground/80">Nexton eCommerce. © 2024</p>
			<div class="flex gap-1">
				<img v-for="icon in paymentIcons" :src="icon" />
			</div>
		</div>
	</footer>
</template>

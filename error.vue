<script setup lang="ts">
import { Button } from "~/components/ui/button";
</script>

<template>
	<div class="flex flex-col items-center justify-center h-screen gap-6">
		<h1 class="text-8xl text-foreground font-bold">404</h1>
		<p class="text-lg text-foreground">Oops! Page not found.</p>
		<Button>
			<NuxtLink to="/">Go home</NuxtLink>
		</Button>
	</div>
</template>

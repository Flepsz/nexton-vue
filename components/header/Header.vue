<script setup lang="ts"></script>

<template>
	<header
		class="sticky top-0 z-50 w-full border-b border-border/40 bg-background/95 backdrop-blur supports-[backdrop-filter]:bg-background/60"
	>
		<div
			class="container flex h-16 max-w-screen-2xl justify-between items-center"
		>
			<Logo />
			<nav class="inline-flex justify-center items-center gap-5">
				<ThemeSwitcher />
			</nav>
		</div>
	</header>
</template>

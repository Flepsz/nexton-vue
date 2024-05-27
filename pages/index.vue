<script setup lang="ts"></script>

<template>
	<Hero search="Roupa preta inverno simples" />
	<div class="container-section">
		<section class="flex flex-col gap-5 xl:gap-10">
			<TitleBicolor
				first="Start exploring."
				second="Good things are waiting for you"
			/>
			<div class="w-[90%] mx-auto">
				<Collections />
			</div>
		</section>
		<section class="flex flex-col gap-5 xl:gap-10">
			<title-bicolor
				first="Recommendations."
				second="Best matching products for you"
			/>
		</section>
	</div>
</template>

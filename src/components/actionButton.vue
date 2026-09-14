<template>


	<a role="button" :href="to"
		:class="[padding, reverse ? 'bg-white text-blue-600 border-blue-600 hover:bg-blue-50 hover:text-blue-700 focus:text-blue-700 focus:border-blue-700' : 'text-white bg-blue-600 border-blue-500 hover:bg-blue-700 hover:text-white focus:text-white focus:border-blue-600 hover:border-blue-600']"
		class="flex items-center justify-center gap-2 text-sm font-medium transition-colors duration-200 border rounded-lg outline-none select-none w-fit focus:outline-none focus:ring-2 focus:ring-blue-400"
		:aria-label="description">

		<span> {{ description }} </span>
	</a>
</template>

<script setup lang="ts">
	defineProps({
		to: { type: String, required: true },
		description: { type: String, default: "" },
		reverse: { type: Boolean, required: false },
	});

	const padding = "p-[0.50rem] px-3";
</script>

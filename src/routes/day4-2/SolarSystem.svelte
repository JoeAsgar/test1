<div
	class="relative h-screen overflow-hidden bg-black bg-gradient-to-b from-black via-purple-900 to-black"
>
	<div class="absolute top-1/2 left-1/2 h-8 w-8 -translate-1/2 rounded-full bg-yellow-200"></div>

	<!-- Mercury -->
	<div
		class="absolute top-1/2 left-1/2 h-12 w-12 -translate-1/2 animate-[spin_6s_infinite] rounded-full border border-gray-200/40"
	>
		<div class="absolute h-2 w-2 translate-0.5 rounded-full bg-orange-500"></div>
	</div>

	<!-- Venus -->
	<div
		class="centered top-1/2 left-1/2 h-18 w-18 -translate-1/2 animate-[spin_9s_infinite] rounded-full border border-gray-200/40"
	>
		<div class="absolute h-2 w-2 translate-0.5 rounded-full bg-orange-500"></div>
	</div>

	<!-- earth  -->
	<div
		class="absolute top-1/2 left-1/2 h-30 w-30 -translate-1/2 animate-[spin_16s_infinite] rounded-full border border-gray-200/40"
	>
		<div
			class="absolute h-2 w-2 translate-[13px] animate-[spin_12s_infinite] rounded-full bg-blue-300 bg-gradient-to-b from-blue-300 via-green-600 to-green-700"
		>
			<div class="h-1 w-1 -translate-[3px] rounded-full bg-white"></div>
		</div>
	</div>

	<!-- mars -->
	<div
		class="absolute top-1/2 left-1/2 h-60 w-60 -translate-1/2 animate-[spin_20s_infinite] rounded-full border border-gray-200/40"
	>
		<div class="absolute h-2 w-2 translate-[31px] rounded-full bg-orange-500"></div>
	</div>

	<!-- Jupiter -->
	<div
		class="absolute top-1/2 left-1/2 h-100 w-100 -translate-1/2 animate-[spin_25s_infinite] rounded-full border border-gray-200/40"
	>
		<div class="absolute h-6 w-6 translate-[46px] rounded-full bg-yellow-500"></div>
	</div>

	<!-- saturn -->
	<div
		class="absolute top-1/2 left-1/2 h-140 w-140 -translate-1/2 animate-[spin_30s_infinite] rounded-full border border-gray-200/40"
	>
		<div class="absolute h-6 w-6 translate-[70px] rounded-full bg-yellow-200"></div>
	</div>
	<!-- Neptune -->
	<div
		class="absolute top-1/2 left-1/2 h-175 w-175 -translate-1/2 animate-[spin_38s_infinite] rounded-full border border-gray-200/40"
	>
		<div class="absolute h-5 w-5 translate-[92px] rounded-full bg-blue-200"></div>
	</div>

	<!-- stars -->

	{#each Array(100) as _, i}
		<div
			class="absolute h-1 w-1 animate-pulse rounded-full bg-white/60"
			style="top: {Math.random() * 90}vh; left: {Math.random() *
				90}vw; animation-delay: {Math.floor(Math.random() * 250)}ms"
		></div>
	{/each}
</div>

<style>
	.centered {
		@apply absolute top-1/2 left-1/2 -translate-1/2;
	}
</style>

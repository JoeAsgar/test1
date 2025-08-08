<script>
	let { emote, position, color, animation } = $props();
</script>

<div class="flex h-10 items-center border bg-gray-700">
	<div
		style=" width:{position}%"
		class="transform-all h-full w-6 shrink-0 duration-1000 {color}"
	></div>
	<div class="animal {animation}">{emote}</div>
</div>

<style>
	.animal {
		font-size: 60px;
	}
	.bounce {
		animation: bounce 2s infinite;
	}
	.spin {
		animation: spin 0.5s infinite;
	}
	.ping {
		animation: ping 1s infinte;
	}
</style>

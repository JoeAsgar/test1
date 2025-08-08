<script>
	let { text, fn } = $props();
</script>

<button
	onclick={fn}
	class="hover:cursur-pointer m-2 rounded border bg-blue-400 px-3 py-1 transition-all duration-200 hover:scale-110 hover:bg-black hover:text-white active:text-green-200"
>
	{text}</button
>

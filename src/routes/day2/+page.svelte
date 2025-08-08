<script>
	import Button from '../../Components/Button.svelte';
	import LoadingBar from '../../Components/LoadingBar.svelte';
	import HorseRace from './HorseRace.svelte';
	let progress = $state(0);

	function increment() {
		progress += 10;
		if (progress > 100) {
			progress = 100;
		}
	}
	function decrement() {
		progress -= 10;
		if (progress < 0) {
			progress = 0;
		}
	}
	function reset() {
		progress = 0;
	}
</script>

<HorseRace />

<Button text={'Reset'} fn={reset} />
<Button text={'Increment'} fn={increment} />
<Button text={'Decrement'} fn={decrement} />
<LoadingBar color={'bg-blue-500'} current={progress} , max={100} />

<div class="bg-red-500 text-center transition-all duration-1000 hover:bg-blue-500 hover:uppercase">
	transition
</div>

<div class="m-2 h-10 w-10 border transition-all duration-100 hover:bg-yellow-200">Box 1</div>
<div
	class="m-2 h-10 w-10 border transition-all duration-100 hover:w-12 hover:rounded-full hover:uppercase"
>
	Box 2
</div>
<div class="m-2 h-10 w-10 border transition-all duration-100 hover:w-100 hover:animate-spin">
	Box 3
</div>
<div class="m-2 h-10 w-10 border transition-all duration-100 hover:scale-110 hover:text-green-300">
	Box 4
</div>

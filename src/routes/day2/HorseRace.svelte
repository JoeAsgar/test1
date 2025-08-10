<script>
	import Button from '../../Components/Button.svelte';
	import Horse from './Horse.svelte';

	let horses = $state([
		{
			emote: '🏇',
			position: 0,
			color: 'bg-yellow-300',
			animation: 'bounce'
			
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-blue-500',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-blue-800',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-blue-400',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-orange-500',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-red-500',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-purple-200',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-black',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-green-700',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-green-500',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-white',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-yellow-500',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-red-800',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-pink-300',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-gradient-to-b from-blue-300 via-orange-400 to-yellow-300',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-lime-500',
			animation: 'bounce'
		}
	]);

	function progress() {
		let maxHorse = horses[0];
		for (let horse of horses) {
			let r = parseInt(Math.random() * 20);
			horse.position += r;
			if (horse.position > 100) {
				horse.position = 100;
			}
			if (horse.position > maxHorse.position) {
				maxHorse = horse;
			}
		}
		for (let horse of horses) {
			if (horse.position == maxHorse.position) {
				horse.animation = 'spin';
			} else {
				horse.animation = 'bounce';
			}
		}
		maxHorse.animation = 'spin';
	}
	function reset() {
		for (let horse of horses) {
			horse.position = 0;
		}
	}
</script>

<div style="height:800px;" class="bg-green-400">
	<div class="py-5 text-center text-2xl font-bold">HORSE RACING GAME</div>
	<Button text={'Progress'} fn={progress} />
	<Button text={'Reset'} fn={reset} />
	<div class="py-10 pr-10">
		{#each horses as horse}
			<Horse
				emote={horse.emote}
				color={horse.color}
				animation={horse.animation}
				position={horse.position}
			/>
		{/each}
	</div>
</div>

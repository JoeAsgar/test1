<script>
	import Button from '../../Components/Button.svelte';
</script>

<div class="w-full bg-yellow-200">
	<div class="prose p-5">
		<h1 class="text-center">Joes Profile</h1>

		<hr />

		<div
			class="profile-image h-20 w-20 overflow-hidden rounded-full bg-black bg-cover bg-center"
		></div>

		<div>Joseph Akbari</div>
		<div>Student</div>

		<h2>About Me</h2>
		<div>Hi my name is Joe.</div>

		<h2>Haiku Excersise</h2>
		<div class="h-7 bg-yellow-100 text-center">Dimwitted you are</div>
		<div class="h-7 bg-yellow-100 text-center">Dung beetles roll forever</div>
		<div class="h-7 bg-yellow-100 text-center">Drool flows from your chin</div>

		<h2>Components</h2>

		<div>
			<Button text={'CLICK ME 🍪'} message={'Good boy'} />
		</div>
		<div>
			<Button text={'DONT CLICK ME 😈'} message={'womp womp'} />
		</div>
	</div>
</div>

<style>
	.profile-image {
		background-image: url('https://images.unsplash.com/photo-1728116693268-125c5d6ad9e2?q=80&w=1529&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
	}
</style>

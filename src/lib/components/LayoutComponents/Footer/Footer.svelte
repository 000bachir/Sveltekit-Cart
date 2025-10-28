<script>
	import Email from '$lib/assets/Icons/Email.svelte';
	import Github from '$lib/assets/Icons/Github.svelte';
</script>

<footer class="relative grid h-32 w-full grid-cols-2 overflow-hidden bg-amber-400">
	<!--github one -->
	<div class=" col-span-1 flex h-full w-full items-center justify-center">
		<a href="/https://github.com/000bachir" class="flex flex-col items-center">
			<div class="">
				<Github width="36" height="36" />
			</div>
			<h1 class="text-lg font-semibold">See my Github</h1>
		</a>
	</div>

	<!--email one-->
	<div class="col-span-1 flex h-full w-full items-center justify-center">
		<a href="https://mail.google.com/mail/?view=cm&to=peakdev698@gmail.com" class="flex flex-col items-center">
			<div class="">
				<Email width="36" height="36" />
			</div>
			<h1 class="text-lg font-semibold">Send me an Email</h1>
		</a>
	</div>
</footer>

<style>
</style>

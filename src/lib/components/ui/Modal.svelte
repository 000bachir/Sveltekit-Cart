<script>
	let { showModal = $bindable(), children, header } = $props();

	let dialog = $state('');

	$effect(() => {
		if (showModal) {
			dialog.showModal();
		}
	});
</script>

<article class="relative flex items-center justify-center">
	<dialog
		bind:this={dialog}
		onclose={() => (showModal = false)}
		onclick={(e) => {
			if (e.target === dialog) dialog.close();
		}}
		class="bg-red-500 h-[80%] aspect-square rounded-2xl "
	>
		<div class="">
			{@render header?.()}
			<hr />
			{@render children?.()}
			<hr />
			<!-- svelte-ignore a11y_autofocus -->
			<button
				autofocus
				title="close"
				onclick={() => dialog.close()}
				class="cursor-pointer bg-linear-to-r from-cyan-500 to-blue-500 text-white"
			>
				<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20"
					><path
						fill="currentColor"
						d="M2.93 17.07A10 10 0 1 1 17.07 2.93A10 10 0 0 1 2.93 17.07M11.4 10l2.83-2.83l-1.41-1.41L10 8.59L7.17 5.76L5.76 7.17L8.59 10l-2.83 2.83l1.41 1.41L10 11.41l2.83 2.83l1.41-1.41L11.41 10z"
					/></svg
				>
			</button>
		</div>
	</dialog>
</article>

<style>
	dialog {
		position: fixed;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		margin: 0; /* Remove default margin */
	}

	dialog::backdrop {
		background: rgba(0, 0, 0, 0.8);
	}

	dialog > div {
		padding: 2rem;
	}

	dialog[open] {
		animation: zoom 500ms ease-in-out;
	}

	@keyframes zoom {
		from {
			transform: scale(0.95);
		}
		to {
			transform: scale(1);
		}
	}
	dialog[open]::backdrop {
		animation: fade 500ms ease-out;
	}

	@keyframes zoom {
		from {
			opacity: 0;
		}
		to {
			opacity: 1;
		}
	}

	button {
		display: flex;
	}
</style>

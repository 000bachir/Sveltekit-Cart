<script>
	let { showModal = $bindable(), children, header , title } = $props();

	let dialog = $state('');


	$effect(() => {
		if (showModal) {
			dialog.showModal();
		}
	});
</script>

<article class=" flex items-center justify-center">
	<dialog
		bind:this={dialog}
		onclose={() => (showModal = false)}
		onclick={(e) => {
			if (e.target === dialog) dialog.close();
		}}
		class="h-auto w-auto overflow-scroll overflow-x-auto rounded-2xl "
	>
		<div class="flex flex-col">
			<div class=" flex w-full items-center justify-between">
				{@render header?.()}
				<h2 class="font-semibold text-white">{title}</h2>
				<button
					autofocus
					title="close"
					onclick={() => dialog.close()}
					class="cursor-pointer overflow-hidden"
				>
					<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20"
						><path
							fill="white"
							d="M2.93 17.07A10 10 0 1 1 17.07 2.93A10 10 0 0 1 2.93 17.07M11.4 10l2.83-2.83l-1.41-1.41L10 8.59L7.17 5.76L5.76 7.17L8.59 10l-2.83 2.83l1.41 1.41L10 11.41l2.83 2.83l1.41-1.41L11.41 10z"
						/></svg
					>
				</button>
			</div>
			<div class="w-auto">
				{@render children?.()}
			</div>
			<!-- svelte-ignore a11y_autofocus -->
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
		background: rgba(255, 255, 255, 0.23);
		backdrop-filter: blur(37px);
		-webkit-backdrop-filter: blur(37px);
		border-radius: 20px;
		border: 1px solid rgba(255, 255, 255, 0.3);
		box-shadow:
			0 8px 32px rgba(0, 0, 0, 0.1),
			inset 0 1px 0 rgba(255, 255, 255, 0.5),
			inset 0 -1px 0 rgba(255, 255, 255, 0.1),
			inset 0 0 0px 0px rgba(255, 255, 255, 0);
	}

	

	dialog::before {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		height: 1px;
		background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.8), transparent);
	}

	dialog::after {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		width: 1px;
		height: 100%;
		background: linear-gradient(
			180deg,
			rgba(255, 255, 255, 0.8),
			transparent,
			rgba(255, 255, 255, 0.3)
		);
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

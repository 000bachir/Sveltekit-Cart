<script>
	let { showModal = $bindable(), children, header } = $props();

	let dialog = $state('');

	$effect(() => {
		if (showModal) {
			dialog.showModal();
		}
	});
</script>

<dialog
	bind:this={dialog}
	onclose={() => (showModal = false)}
	onclick={(e) => {
		if (e.target === dialog) dialog.close();
	}}
>
	<div class="">
		{@render header?.()}
		<hr />
		{@render children?.()}
		<hr />
		<!-- svelte-ignore a11y_autofocus -->
		<button autofocus onclick={() => dialog.close()}> Close </button>
	</div>
</dialog>

<style>
	dialog {
		/* max-width:32rem; */
        background: red;
		width: 100%;
		max-width: 420px;
		max-height: 20rem;
		border: none;
		overflow-y: scroll;
		box-shadow:
			rgba(6, 24, 44, 0.4) 0px 0px 0px 2px,
			rgba(6, 24, 44, 0.65) 0px 4px 6px -1px,
			rgba(255, 255, 255, 0.08) 0px 1px 0px inset;
        padding: 1rem;
        overflow: hidden;
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
		display: block;
	}
</style>

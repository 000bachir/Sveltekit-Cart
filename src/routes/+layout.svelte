<script>
	import '../app.css';
	import Cart from "$lib/assets/Cart.svg"
	import Navbar from '$lib/components/LayoutComponents/Navbar/Navbar.svelte';
	import Footer from '$lib/components/LayoutComponents/Footer/Footer.svelte';
	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={Cart} />
</svelte:head>


<header class="h-auto w-full relative overflow-hidden">
	<Navbar />
</header>
{@render children?.()}

<Footer />
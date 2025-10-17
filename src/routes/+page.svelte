<script>
    import Hero from "$lib/components/UI/Hero.svelte";
</script>

<svelte:head>
    <title>
        Shopping Cart
    </title>
    <meta name="description" content="A developer blog sharing tutorials and projects built with SvelteKit, JavaScript, and modern web technologies." />
</svelte:head>

<main class="h-auto w-full relative overflow-hidden">
    <section id="title_of_the_blog" class="h-28 w-full relative overflow-hidden bg-amber-400 flex items-center justify-center">
        <h1 class="font-semibold 2xl:text-3xl xl:text-2xl lg:text-xl md:text-lg sm:text-sm  underline decoration-4">
            The Easiest Way to Make a Cart in SvelteKit
        </h1>
    </section>

    <section class="">
        <Hero />
    </section>
</main>
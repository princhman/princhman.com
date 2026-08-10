<script lang="ts">
    let { children } = $props();
</script>

<svelte:head>
    <meta name="theme-color" content="#151515" />
</svelte:head>

<div class="min-h-screen bg-[#151515] text-white selection:bg-[#d9ff72] selection:text-black">
    <header class="border-b border-white/10">
        <div class="mx-auto flex max-w-3xl items-center justify-between px-5 py-5 sm:px-8">
            <a href="/" class="text-sm text-white/55 transition hover:text-white">princhman.com</a>
            <a href="/tiempo/support" class="text-sm text-white/55 transition hover:text-white">Tiempo support</a>
        </div>
    </header>

    {@render children()}
</div>

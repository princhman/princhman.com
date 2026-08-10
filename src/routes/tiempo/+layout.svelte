<script lang="ts">
    let { children } = $props();
</script>

<svelte:head>
    <meta name="theme-color" content="#151515" />
</svelte:head>

<div
    class="flex min-h-screen flex-col bg-[#151515] text-white selection:bg-[#d9ff72] selection:text-black"
>
    <header>
        <div
            class="mx-auto flex max-w-3xl items-center justify-between px-5 py-5 sm:px-8"
        >
            <a
                href="/tiempo"
                class="flex items-center gap-3 text-white transition hover:opacity-75"
            >
                <img
                    src="/tiempo-icon.png"
                    alt=""
                    class="h-9 w-9 rounded-[28%]"
                />
                <span class="text-sm font-semibold">Tiempo</span>
            </a>
            <div class="flex gap-3">
                <a
                    href="/tiempo/privacy"
                    class="text-sm text-white/55 transition hover:text-white"
                    >Privacy</a
                >
                <a
                    href="/tiempo/support"
                    class="text-sm text-white/55 transition hover:text-white"
                    >Support</a
                >
            </div>
        </div>
    </header>

    <div class="flex flex-1 flex-col">
        {@render children()}
    </div>
</div>

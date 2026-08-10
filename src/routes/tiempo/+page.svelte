<script lang="ts">
    // Add the public App Store listing URL here once the app is available.
    const appStoreUrl = "";
</script>

<svelte:head>
    <title>Tiempo — Private activity tracking</title>
    <meta
        name="description"
        content="Tiempo is a private activity and time tracker for iPhone, iPad, and Mac."
    />
</svelte:head>

<main class="mx-auto flex min-h-[calc(100vh-65px)] max-w-3xl flex-col justify-center px-5 py-16 sm:px-8">
    <div class="grid items-center gap-10 sm:grid-cols-[160px_1fr] sm:gap-14">
        <img
            src="/tiempo-icon.png"
            alt="Tiempo app icon"
            class="h-32 w-32 rounded-[28%] shadow-[0_24px_70px_rgba(0,0,0,0.45)] sm:h-40 sm:w-40"
        />

        <div>
            <p class="mb-4 text-xs font-semibold uppercase tracking-[0.2em] text-[#d9ff72]">
                Your time, privately
            </p>
            <h1 class="text-5xl font-semibold tracking-tight sm:text-6xl">Tiempo</h1>
            <p class="mt-6 max-w-xl text-lg leading-8 text-white/60">
                A calm activity and time tracker for iPhone, iPad, and Mac. Track what matters,
                understand where your time goes, and keep everything in sync through your private iCloud.
            </p>

            <div class="mt-9">
                {#if appStoreUrl}
                    <a
                        href={appStoreUrl}
                        class="inline-flex min-h-14 items-center rounded-xl border border-white/15 bg-white px-5 text-black transition hover:bg-[#d9ff72]"
                    >
                        <span class="text-sm font-semibold">Download on the App Store</span>
                    </a>
                {:else}
                    <span
                        aria-disabled="true"
                        class="inline-flex min-h-14 cursor-default items-center rounded-xl border border-white/10 bg-white/[0.04] px-5 text-white/45"
                    >
                        <span class="text-sm font-semibold">Coming to the App Store</span>
                    </span>
                {/if}
            </div>
        </div>
    </div>

    <footer class="mt-20 flex gap-6 border-t border-white/10 pt-6 text-sm text-white/45 sm:ml-[214px]">
        <a href="/tiempo/privacy" class="transition hover:text-white">Privacy</a>
        <a href="/tiempo/support" class="transition hover:text-white">Support</a>
    </footer>
</main>

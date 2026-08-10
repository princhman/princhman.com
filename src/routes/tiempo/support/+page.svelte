<svelte:head>
    <title>Tiempo Support</title>
    <meta
        name="description"
        content="Help and contact information for Tiempo on iPhone, iPad, and Mac."
    />
</svelte:head>

<main class="mx-auto max-w-3xl px-5 py-16 sm:px-8 sm:py-24">
    <div class="max-w-2xl">
        <p class="mb-4 text-xs font-semibold uppercase tracking-[0.2em] text-[#d9ff72]">Tiempo</p>
        <h1 class="text-4xl font-semibold tracking-tight sm:text-5xl">Support</h1>
        <p class="mt-6 text-lg leading-8 text-white/60">
            Tiempo is a private activity and time tracker for iPhone, iPad, and Mac. If something is not
            working or you have a question, send an email and include the device and OS version you are using.
        </p>
    </div>

    <div class="mt-14 grid gap-4 sm:grid-cols-2">
        <a
            href="mailto:princhman@icloud.com?subject=Tiempo%20support"
            class="group rounded-2xl border border-white/10 bg-white/[0.03] p-6 transition hover:border-[#d9ff72]/50 hover:bg-white/[0.06]"
        >
            <p class="text-sm text-white/45">Email support</p>
            <p class="mt-2 text-lg text-white group-hover:text-[#d9ff72]">princhman@icloud.com</p>
            <p class="mt-5 text-sm text-white/40">We aim to reply within a few working days.</p>
        </a>

        <a
            href="/tiempo/privacy"
            class="group rounded-2xl border border-white/10 bg-white/[0.03] p-6 transition hover:border-[#d9ff72]/50 hover:bg-white/[0.06]"
        >
            <p class="text-sm text-white/45">Your data</p>
            <p class="mt-2 text-lg text-white group-hover:text-[#d9ff72]">Read the privacy policy</p>
            <p class="mt-5 text-sm text-white/40">How Tiempo stores, syncs, and protects activity data.</p>
        </a>
    </div>

    <section class="mt-16 border-t border-white/10 pt-10 text-white/60">
        <h2 class="text-xl font-semibold text-white">Before contacting support</h2>
        <ul class="mt-5 list-disc space-y-3 pl-5 leading-7 marker:text-[#d9ff72]">
            <li>Check that you are signed into the same iCloud account on devices you want to sync.</li>
            <li>Allow Local Network access for faster sync between nearby devices.</li>
            <li>Keep Tiempo updated on each device.</li>
        </ul>
    </section>
</main>

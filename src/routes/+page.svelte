<script lang="ts">
    type Project = {
        name: string;
        url: string;
        description: string;
        icon?: string;
        github?: string;
        builtOn?: { name: string; url: string; icon: string };
    };

    const socials = [
        { name: "X", url: "https://x.com/princh_man", icon: "/x.svg" },
        {
            name: "LinkedIn",
            url: "https://www.linkedin.com/in/vladyslav-nalyvaiko-a0aa6b292/",
            icon: "/linkedin.svg",
        },
        {
            name: "GitHub",
            url: "https://github.com/princhman",
            icon: "/github.svg",
        },
    ];

    const projects: Project[] = [
        {
            name: "Memnoter",
            url: "https://memnoter.com",
            icon: "/memnoter-icon.png",
            github: "https://github.com/princhman/memnoter",
            description:
                "Local-first notes app with spaced-repetition flashcards built into the text. Free and open source",
        },
        {
            name: "Flashies",
            url: "https://flashies.app",
            icon: "/flashies-icon.png",
            description:
                "Language flashcards with translations, pronunciation, and two-way practice to help new words stick",
        },
        {
            name: "Quextro Database",
            url: "https://quextro.princhman.com",
            icon: "/quextro.png",
            description:
                "Biggest available question database for UK high-school exams. With filters, completions, and online notebooks",
        },
        {
            name: "Quextro Planner",
            url: "https://planner.quextro.com",
            icon: "/quextro.png",
            description: "Study planner with spaced repetition",
        },
        {
            name: "Needline",
            url: "https://needline.princhman.com",
            icon: "/needline-logo.svg",
            github: "https://github.com/princhman/needline",
            description:
                "Open source self-hostable customer portal built on",
            builtOn: {
                name: "Linear",
                url: "https://linear.app",
                icon: "/linear-logo.svg",
            },
        },
        {
            name: "Top Dog",
            url: "https://www.topdogtrainingandwelfare.co.uk",
            icon: "/topdog.png",
            description:
                "Website and admin panel built for a dog training business in Surrey",
        },
    ];

    const remakes: Project[] = [
        {
            name: "London Startups",
            url: "https://lsm.princhman.com",
            description:
                "Unofficial redesign of London Startup Map, using its data: search by area, founder or open role, and a list that follows the map",
        },
        {
            name: "Getricher",
            url: "https://getricher.princhman.com",
            description:
                "Multiplayer remake of richup.io, with a Trade Routes mode of my own: no dice, branching routes, deliveries and auctions",
        },
        {
            name: "Tradewind",
            url: "https://tradewind.princhman.com",
            description:
                "Island-building game to play with friends, inspired by Catan",
        },
    ];

    const link =
        "underline decoration-line decoration-1 underline-offset-4 transition-colors duration-150 hover:decoration-fg";
    const icon =
        "invert opacity-50 transition-opacity duration-150 hover:opacity-100";
</script>

<svelte:head>
    <title>Vlad Nalyvaiko</title>
</svelte:head>

{#snippet section(title: string, items: Project[])}
    <section class="pt-16">
        <h2 class="font-medium">{title}</h2>
        <ul class="flex flex-col gap-5 pt-5">
            {#each items as item (item.name)}
                <li class="grid gap-x-6 gap-y-1 sm:grid-cols-[11rem_1fr]">
                    <div class="flex h-6 items-center gap-2.5">
                        {#if item.icon}
                            <img
                                src={item.icon}
                                class="size-5 rounded-sm object-contain"
                                alt=""
                            />
                        {/if}
                        <a href={item.url} class={link}>{item.name}</a>
                    </div>
                    <div class="flex items-start justify-between gap-4">
                        <p class="text-pretty text-muted">
                            {item.description}
                            {#if item.builtOn}
                                <a
                                    href={item.builtOn.url}
                                    class="{link} whitespace-nowrap text-fg"
                                    >{item.builtOn.name}<img
                                        src={item.builtOn.icon}
                                        class="ml-1 inline size-3"
                                        alt=""
                                    /></a
                                >
                            {/if}
                        </p>
                        {#if item.github}
                            <a
                                href={item.github}
                                aria-label="{item.name} on GitHub"
                                class="-m-2 shrink-0 p-2"
                            >
                                <img
                                    src="/github.svg"
                                    class="size-4 translate-y-1 {icon}"
                                    alt=""
                                />
                            </a>
                        {/if}
                    </div>
                </li>
            {/each}
        </ul>
    </section>
{/snippet}

<main
    class="mx-auto min-h-screen w-full max-w-2xl px-5 pt-12 pb-20 font-sans text-[15px] leading-6 text-fg antialiased sm:pt-20"
>
    <header class="flex items-center justify-between gap-4">
        <div class="flex items-center gap-4">
            <img
                src="/photo.jpeg"
                class="size-16 rounded-lg object-cover"
                alt="Vlad Nalyvaiko"
            />
            <div>
                <h1 class="font-medium">Vlad Nalyvaiko 🇺🇦</h1>
                <p class="text-muted">aka princhman</p>
            </div>
        </div>
        <nav class="-mr-2 flex">
            {#each socials as social (social.name)}
                <a href={social.url} aria-label={social.name} class="p-2">
                    <img src={social.icon} class="size-4 {icon}" alt="" />
                </a>
            {/each}
        </nav>
    </header>

    <p class="pt-10 text-pretty">
        I am learning by building, to become a product-centred engineer,
        focusing on software craftsmanship and UI performance. I love thoughtful
        designs.
    </p>

    {@render section("Projects", projects)}
    {@render section("Remakes", remakes)}

    <section class="pt-16">
        <h2 class="font-medium">Education</h2>
        <div class="flex items-center justify-between gap-4 pt-5">
            <div class="flex items-center gap-2.5">
                <img src="/ucl.png" class="-ml-1.5 h-7" alt="UCL" />
                <p>BSc Computer Science</p>
            </div>
            <p class="shrink-0 tabular-nums text-muted">2025 – 2028</p>
        </div>
    </section>
</main>

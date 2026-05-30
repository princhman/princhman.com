<script lang="ts">
    import "./layout.css";

    let { children } = $props();
</script>

<svelte:head>
    <link rel="icon" href="/photo-small.jpeg" />
</svelte:head>
{@render children()}

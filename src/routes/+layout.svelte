<script lang="ts">
    import "./layout.css";
    import favicon from "$lib/assets/favicon.svg";
    import { page } from "$app/state";
    import { Navbar, NavLi, NavUl } from "flowbite-svelte";

    let activeUrl = $derived(page.url.pathname);
    let { children } = $props();
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

<Navbar class="bg-surface border-b-border-warm">
    <NavUl {activeUrl}>
        <NavLi href="/dashboard">Dashboard</NavLi>
        <NavLi href="/transaction">Transaction</NavLi>
        <NavLi href="/reconciliation">Reconciliation</NavLi>
        <NavLi href="/settings">Settings</NavLi>
    </NavUl>
</Navbar>

<main class="flex-1 flex overflow-hidden px-8 py-8 bg-brand-bg">
    {@render children()}
</main>

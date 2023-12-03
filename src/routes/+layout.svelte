<script lang="ts">
    import MainMenu from '$lib/components/MainMenu.svelte';
    import type { MenuItem } from '$lib/types';

    let menuItems: MenuItem[] = [
        { label: 'B&B', link: '/b-and-b' },
        { label: 'Cottage', link: '/cottage' },
        { label: 'Facilities', link: '/facilities' },
        { label: 'Weddings', link: '/weddings' },
    ];
</script>

<header>
    <div class="top"></div>
    <div class="center">
        <MainMenu {menuItems}/>
        <div id="branding">
            <div class="logo"></div>
        </div>
    </div>
</header>

<main>
    <div class="container">
        <slot/>
    </div>
</main>


<footer>
</footer>

<style>
    @import '$lib/global.css';

    header {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        z-index: 999;
    }

    .container {
        position: relative;
        z-index: 1;
        padding: 0 var(--side-padding);
    }
</style>
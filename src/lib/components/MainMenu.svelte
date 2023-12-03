<script lang="ts">
    import type { MenuItem } from '$lib/types';

    export let menuItems: MenuItem[] = [];
</script>

<style>
    nav {
        padding: 1rem;
        text-align: center;
    }

    ul {
        list-style-type: none;
        padding: 0;
        margin: 0;
        display: flex;
        justify-content: center;
    }

    li {
        margin: 0 1rem;
    }

    a {
        color: #fff;
        text-decoration: none;
        font-weight: bold;
        font-size: 1.2rem;
    }
</style>

<nav>
    <ul>
        {#each menuItems as { label, link }}
            <li>
                <a href={link}>{label}</a>
            </li>
        {/each}
    </ul>
</nav>

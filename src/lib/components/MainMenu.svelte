<script lang="ts">
    import type { MenuItem } from '$lib/types';

    export let menuItems: MenuItem[] = [];
</script>

<style lang="scss">
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
    text-decoration: none;
    font-weight: bold;
    font-size: 1.2rem;
    color: var(--color-menu);
    transition: color 0.2s ease-in-out;
    &:hover {
      color: var(--color-menu-hover);
    }
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

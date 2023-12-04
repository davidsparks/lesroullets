<script lang="ts">
    import MainMenu from '$lib/components/MainMenu.svelte';
    import type { MenuItem } from '$lib/types';
    import { page } from '$app/stores';

    let menuItems: MenuItem[] = [
        { label: 'B&B', link: '/b-and-b' },
        { label: 'Cottage', link: '/cottage' },
        { label: 'Facilities', link: '/facilities' },
        { label: 'Weddings', link: '/weddings' },
        { label: 'Wine', link: '/wine' },
    ];

</script>

<header class:reverse={$page.route.id === '/'}>
    <div class="container">
        <!-- Top header, with address, phone number and email address -->
        <div class="top">
            <div class="left">
                <!-- Phone and email address -->
                <div class="contact">
                    <a href="tel:+33490712188">+33 (0)4 90 71 21 88</a>
                    <span class="pipe">|</span>
                    <a href="mailto:info@lesroullets.com">info@lesroullets.com</a>
                </div>
            </div>
            <div class="right">
                <!-- Book now button  -->
                <div class="book-now">
                    <a class="button" href="https://www.booking.com/hotel/fr/les-roullets.fr.html" target="_blank"
                       rel="noopener">
                        Book now
                    </a>
                </div>
            </div>
        </div>
        <!-- Main header, with logo and main menu -->
        <div class="bottom">
            <div class="left">
                <!-- Main menu -->
                <div class="main-menu">
                    <MainMenu {menuItems}/>
                </div>
            </div>
            <div class="center">
                <!-- Logo image linked to homepage -->
                <a href="/" class="logo">
                    <object data="images/logo/DLR-square-white.svg" type="image/svg+xml" title="logo"></object>
                </a>
            </div>
            <div class="right">
                <!-- Language switcher -->
                <div class="language-switcher">
                    <a href="/en">English</a>
                    <span class="pipe">|</span>
                    <a href="/fr">Français</a>
                </div>
            </div>
        </div>
    </div>
</header>

<main>
    <div class="container">
        <slot/>
    </div>
</main>

<footer>
    <div class="container">
    </div>
</footer>

<style lang="scss">
  .container {
    position: relative;
    z-index: 1;
    padding: 0 var(--side-padding);
  }

  header {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    z-index: 999;

    .top {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0.25rem 0;
      position: relative;

      &:after {
        content: '';
        position: absolute;
        bottom: 0;
        left: calc(var(--side-padding) * -0.5);
        right: calc(var(--side-padding) * -0.5);
        border-bottom: 0.5px solid var(--color-border);
      }
    }

    .bottom {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0.5rem 0;

      .left,
      .right {
        flex: 1; /* Distribute available space equally between left and right elements */
        display: flex;
        align-items: center; /* Center items vertically within left and right elements */
      }

      .right {
        justify-content: end;
      }

      .center {
        margin: 0 auto;

        .logo {
          display: inline-block;
          width: 100px;
          height: 100px;
          @include mq($from: md) {
            width: 150px;
            height: 150px;
          }
          @include mq($from: lg) {
            width: 200px;
            height: 200px;
          }
          object {
            object-fit: contain;
            width: 100%;
            height: 100%;
          }
        }
      }
    }
  }

  .contact {

  }

  /*** Call to action link styled as a large white button ***/
  .book-now {
    display: flex;
    justify-content: center;
    align-items: center;

    .button {
      background-color: var(--color-button-background);
      color: var(--color-button-text);
      font-size: 1.2rem;
      padding: 0.5rem 1rem;
      border-radius: 0.5rem;
      border: 1px solid var(--color-black);
      transition: all 0.2s ease-in-out;

      &:hover {
        background-color: var(--color-button-background-hover);
        color: var(--color-button-text-hover);
      }
    }
  }
</style>

















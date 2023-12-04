<script lang="ts">
    import Carousel from '$lib/components/Carousel.svelte';
    import '$lib/styles/global.scss';
</script>

<svelte:head>
    <title>Domaine Les Roullets | Luxury accommodation and vineyard</title>
    <meta name="description"
          content="Domaine Les Roullets is a boutique bed and breakfast and vineyard situated in Provence's Luberon valley."/>
</svelte:head>

<section class="top">
    <div class="container">
        <div class="center">
            <h1>Luxury accommodation and vineyard in Provence's Luberon valley</h1>
        </div>
    </div>
</section>

<section class="image-links">
    <div class="container">
        <div class="row">
            <div class="col">
                <a href="/accommodation">
                    <img src="/images/links/accommodation.jpg" alt="Accommodation"/>
                    <h2>Accommodation</h2>
                </a>
            </div>
            <div class="col">
                <a href="/vineyard">
                    <img src="/images/links/vineyard.jpg" alt="Vineyard"/>
                    <h2>Vineyard</h2>
                </a>
            </div>
            <div class="col">
                <a href="/region">
                    <img src="/images/links/region.jpg" alt="Region"/>
                    <h2>Region</h2>
                </a>
            </div>
            <div class="col">
                <a href="/gallery">
                    <img src="/images/links/gallery.jpg" alt="Gallery"/>
                    <h2>Gallery</h2>
                </a>
            </div>
            <div class="col">
                <a href="/contact">
                    <img src="/images/links/contact.jpg" alt="Contact"/>
                    <h2>Contact</h2>
                </a>
            </div>
        </div>
</section>

<section class="image-carousel">
    <Carousel/>
</section>

<style lang="scss">

  section.top {
        background-color: #000000;
        background-image: url('/images/backgrounds/DSC_6011-Pano.jpg');
        background-size: cover;
        background-position: center;
        height: 100vh;
        transition: background 0.3s, border 0.3s, border-radius 0.3s, box-shadow 0.3s;
        width: 100vw;
        position: relative;
        left: calc(50% - 50vw);
        .container {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            .center {
                display: flex;
                flex-wrap: wrap;
                max-width: 960px;
                margin: 20vh auto 0;
                align-items: center;
              h1 {
                font-size: 72px;
                color: white;
                text-align: center;
                //@media screen and (max-width: var(--width-md)) {
                //  font-size: 48px;
                //}
                @media (max-width: 600px) {
                  font-size: 48px;
                }
              }
            }
        }
    }

</style>
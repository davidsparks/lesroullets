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
    <div class="center">
        <h2>Luxury accommodation and vineyard in Provence's Luberon valley</h2>
    </div>
</section>

<style>
    section.top {
        background-color: #000000;
        background-image: url('/images/DSC_6011-Pano.jpg');
        background-size: cover;
        background-position: center;
        height: 100vh;
        transition: background 0.3s, border 0.3s, border-radius 0.3s, box-shadow 0.3s;
        width: 100vw;
        position: relative;
        left: calc(50% - 50vw);
    }
    section.top .container {
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
    }
    section.top .center {
        display: flex;
        flex-wrap: wrap;
        max-width: 960px;
        margin: 0 auto;
        align-items: center;
        height: 50vh;
    }
    h1 {
        font-size: 72px;
        color: white;
        text-align: center;
    }
</style>
<!--
  Carousel.svelte
  This Svelte component is responsible for rendering a carousel of images.
-->
<script lang="ts">
</script>

<div class="carousel">
    <!-- Five slides, each with an image linked to another page on the site -->
    <div class="carousel__inner">
        <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank" class="carousel__slide carousel__slide--current">
            <img src="https://i.imgur.com/5ZQqZ5u.jpg" alt="Slide 1" />
        </a>
        <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank" class="carousel__slide carousel__slide--previous">
            <img src="https://i.imgur.com/5ZQqZ5u.jpg" alt="Slide 2" />
        </a>
        <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank" class="carousel__slide">
            <img src="https://i.imgur.com/5ZQqZ5u.jpg" alt="Slide 3" />
        </a>
        <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank" class="carousel__slide carousel__slide--next">
            <img src="https://i.imgur.com/5ZQqZ5u.jpg" alt="Slide 4" />
        </a>
        <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank" class="carousel__slide">
            <img src="https://i.imgur.com/5ZQqZ5u.jpg" alt="Slide 5" />
        </a>
    </div>
</div>

<style lang="scss">
  .carousel {
    position: relative;
    width: 100%;
    height: 100%;
    overflow: hidden;
  }

  .carousel__inner {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
  }

  .carousel__slide {
    position: relative;
    flex: 1 0 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #eee;
    font-size: 100px;
    font-weight: bold;
    color: #fff;
    text-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
    transform-origin: center center;
    will-change: transform;
  }

  .carousel__slide--current {
    z-index: 1;
  }

  .carousel__slide--previous,
  .carousel__slide--next {
    z-index: 0;
    transform: scale(0.8);
  }

  .carousel__slide--previous {
    transform-origin: left center;
  }

  .carousel__slide--next {
    transform-origin: right center;
  }
</style>

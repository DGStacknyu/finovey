<script lang="ts">
  import { Splide, SplideSlide } from "@splidejs/svelte-splide";
  import "@splidejs/svelte-splide/css";
  import about from "$lib/images/about.png";
  import girl from "$lib/images/girl.png";
</script>

<section class="mx-2">
  <Splide
    options={{
      rewind: true,
      autoplay: true,
      arrows: false,
      perPage: 1,

      gap: "4rem",
      breakpoints: {
        640: {
          perPage: 2,
        },
        768: {
          perPage: 3,
        },
        1024: {
          perPage: 4,
        },
      },
    }}
    aria-label="Banners"
    class="mx-auto h-full w-full"
  >
    <SplideSlide>
      <a href="/" class="">
        <img
          src={about}
          class="h-auto w-auto object-cover transition-all duration-300"
          alt=""
        />
      </a>
    </SplideSlide>
    <SplideSlide>
      <a href="/" class="">
        <img
          src={girl}
          class=" object-cover transition-all duration-300"
          alt=""
        />
      </a>
    </SplideSlide>
  </Splide>
</section>

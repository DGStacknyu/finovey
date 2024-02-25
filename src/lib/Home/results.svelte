<script lang="ts">
  import Icon from "@iconify/svelte";
  import Resultcard from "$lib/Home/resultCard.svelte";
  import ResultCard from "$lib/Home/resultCard.svelte";
</script>

<section class="lg:px-10 px-4 md:py-20 py-10 bg-[#f5f2f0]">
  <div
    class=" md:py-8 grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 lg:place-items-end text-black gap-6"
  >
    <h1 class="md:text-5xl text-4xl font-semibold">
      Tangible results shared here
    </h1>
    <p class=" md:text-xl text-lg font-semibold">
      Discover how our financial expertise transformed businesses like yours,
      delivering exceptional results and growth.
    </p>
    <button
      class="w-fit relative overflow-hidden bg-black text-white px-8 py-4 text-lg font-semibold transition-all duration-300 transform-gpu group"
    >
      <span
        class="absolute inset-0 bg-white transform translate-y-full group-hover:translate-y-0 transition-transform duration-300"
      ></span>
      <span class="relative z-10 group-hover:text-black"
        >Read all testimonials</span
      >
    </button>
  </div>
  <div class="grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 mt-14 gap-8">
    <ResultCard />
    <ResultCard />
    <ResultCard />
  </div>
</section>

<script lang="ts">
  import Icon from "@iconify/svelte";
  import Customercard from "./customercard.svelte";
</script>

<section class="lg:px-10 px-4 md:py-20 py-10 bg-[#052E26]">
  <div
    class=" py-8 grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 lg:place-items-end gap-6 text-white"
  >
    <h1 class="md:text-5xl text-4xl font-semibold">
      Our customer success stories
    </h1>
    <p class="md:text-xl text-lg font-semibold">
      Discover how businesses like yours transformed with our software. Real
      stories of growth, innovation, and success.
    </p>
    <button
      class="mt-5 lg:mt-0 w-fit relative overflow-hidden bg-black text-white px-8 py-4 text-lg font-semibold transition-all duration-300 transform-gpu group"
    >
      <span
        class="absolute inset-0 bg-white transform translate-y-full group-hover:translate-y-0 transition-transform duration-300"
      ></span>
      <span class="relative z-10 group-hover:text-black">View Case studies</span
      >
    </button>
  </div>
  <div class="grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 mt-14 gap-8">
    <Customercard />
    <Customercard />
    <Customercard />
  </div>
</section>

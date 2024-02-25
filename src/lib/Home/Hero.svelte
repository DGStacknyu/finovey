<script lang="ts">
  import Icon from "@iconify/svelte";
  import about from "$lib/images/about.png";
  import HeroSlider from "./HeroSlider.svelte";
</script>

<section class="grid lg:grid-cols-2 bg-[#F5F2F0] grid-cols-1">
  <div class="lg:p-14 md:p-8 p-5">
    <p class="text-xl bg-white w-fit px-2 py-1">Financial services</p>
    <h1
      class="lg:text-6xl md:text-5xl text-4xl font-semibold mt-5 lg:leading-[4.5rem]"
    >
      Build a sustainable future for your company
    </h1>
    <p class="text-xl mt-5 font-medium">
      Unlock success with tailored financial consulting solutions for your
      business growth.
    </p>
    <div class="flex gap-3 mt-6">
      <button
        class="relative overflow-hidden bg-black text-white px-8 py-4 text-lg font-semibold transition-all duration-300 transform-gpu group"
      >
        <span
          class="absolute inset-0 bg-white transform translate-y-full group-hover:translate-y-0 transition-transform duration-300"
        ></span>
        <span class="relative z-10 group-hover:text-black"
          >Free consultation</span
        >
      </button>

      <div class="flex justify-between items-center">
        <Icon
          icon="lets-icons:video-fill"
          class="w-16 h-16 text-black hover:text-black transition-colors duration-300"
        />
        <p class="text-xl font-medium">watch video</p>
      </div>
    </div>
  </div>
  <!-- <img src={about} alt="" class="h-full w-full object-cover" /> -->
  <HeroSlider />
</section>

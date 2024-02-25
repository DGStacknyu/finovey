<script>
  import Icon from "@iconify/svelte";
  import Logo from "$lib/images/about.png";
  const cards = [
    {
      id: "financialPlanning",
      title: "Financial planning",
      mainTitle: "Strategic planning for optimal growth",
      subtitle:
        "Crafting precise financial roadmaps aligned with your business objectives.",
      points: [
        "Optimize resource allocation",
        "Adapt to market changes",
        "Achieve long-term goals",
      ],
    },
    {
      id: "performanceAnalysis",
      title: "Performance analysis",
      mainTitle: "In-depth financial performance analysis",
      subtitle:
        "Analyze and enhance financial performance for sustained growth",
      points: [
        "Identify strengths and weaknesses",
        "Optimize operational efficiency ",
        "Increase revenue streams",
      ],
    },
    {
      id: "investmentAdvisory",
      title: "Investment advisory",
      mainTitle: "Expert advisory tailored for maximum returns",
      subtitle:
        "Tailored investment strategies for optimal returns and risk management",
      points: [
        "Capitalize on market opportunities ",
        "Minimize investment risks",
        "Realize growth potential ",
      ],
    },
  ];

  let selectedCard = null;

  function navigateToCard(index) {
    selectedCard = index;
    const element = document.getElementById(cards[index].id);
    if (element) {
      element.scrollIntoView({ behavior: "smooth" });
    }
  }
</script>

<section class="border-b-2 border-gray-300">
  <div
    class=" py-8 text-lg font-semibold grid lg:grid-cols-3 place-items-center md:grid-cols-2 grid-cols-1 gap-5"
  >
    {#each cards as card, i}
      <div
        class="cursor-pointer transition-colors duration-300 hover:text-gray-900 hover:underline focus:underline focus:text-gray-900"
        on:click={() => navigateToCard(i)}
      >
        <div
          class={i === selectedCard
            ? "text-gray-900 underline"
            : "text-gray-500"}
        >
          {card.title}
        </div>
      </div>
    {/each}
  </div>
  <div class="grid lg:grid-cols-2 grid-cols-1 md:space-y-16">
    {#each cards as card, i}
      {#if i % 2 === 0}
        <!-- Even index: Content at left, image at right -->
        <div class="lg:p-14 p-6" id={card.id}>
          <p class="text-xl bg-[#F5F2F0] w-fit px-2 py-1">{card.title}</p>
          <h1 class="md:text-5xl text-4xl mt-5 leading-[4.5rem]">
            {card.mainTitle}
          </h1>
          <p class="text-xl mt-5 font-medium">{card.subtitle}</p>
          <div class="mt-6 space-y-3">
            {#each card.points as point}
              <div class="flex items-center gap-2">
                <div class="bg-[#F5F2F0] w-10 h-10">
                  <Icon icon="material-symbols:check" class="w-10 h-10" />
                </div>
                <p class="text-xl font-medium">{point}</p>
              </div>
            {/each}
          </div>
          <button
            class="mt-10 relative overflow-hidden bg-black text-white px-8 py-4 text-lg font-semibold transition-all duration-300 transform-gpu group"
          >
            <span
              class="absolute inset-0 bg-white transform translate-y-full group-hover:translate-y-0 transition-transform duration-300"
            ></span>
            <span class="relative z-10 group-hover:text-black">Learn More</span>
          </button>
        </div>
        <div class="hidden lg:block">
          <img src={Logo} alt="" class="h-full w-full object-cover p-4" />
        </div>
      {/if}
      {#if i % 2 !== 0}
        <!-- Odd index: Image at left, content at right -->
        <div class="hidden lg:block">
          <img src={Logo} alt="" class="h-full w-full object-cover p-4" />
        </div>
        <div class="lg:p-14 p-6" id={card.id}>
          <p class="text-xl bg-[#F5F2F0] w-fit px-2 py-1">{card.title}</p>
          <h1 class="md:text-5xl text-4xl mt-5 leading-[4.5rem]">
            {card.mainTitle}
          </h1>
          <p class="text-xl mt-5 font-medium">{card.subtitle}</p>
          <div class="mt-6 space-y-3">
            {#each card.points as point}
              <div class="flex items-center gap-2">
                <div class="bg-[#F5F2F0] w-10 h-10">
                  <Icon icon="material-symbols:check" class="w-10 h-10" />
                </div>
                <p class="text-xl font-medium">{point}</p>
              </div>
            {/each}
          </div>
          <button
            class="mt-10 relative overflow-hidden bg-black text-white px-8 py-4 text-lg font-semibold transition-all duration-300 transform-gpu group"
          >
            <span
              class="absolute inset-0 bg-white transform translate-y-full group-hover:translate-y-0 transition-transform duration-300"
            ></span>
            <span class="relative z-10 group-hover:text-black">Learn More</span>
          </button>
        </div>
      {/if}
      <!-- For mobile, display image before content -->
      <div class="lg:hidden">
        <img src={Logo} alt="" class="h-full w-full object-cover p-4" />
      </div>
    {/each}
  </div>
</section>

<style>
  .underline {
    position: relative;
    display: inline-block;
    padding-bottom: 3px;
  }

  .underline::after {
    content: "";
    position: absolute;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 2px;
    background-color: #333;
  }
</style>

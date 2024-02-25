<script lang="ts">
  import Icon from "@iconify/svelte";

  let selectedData =
    "We embody unwavering expertise, garnered through years of industry mastery. Our team’s extensive knowledge and refined skills ensure effective solutions, fostering trust and delivering excellence.";

  let buttons = [
    {
      id: 1,
      text: "Expertise",
      selected: true,
      data: "We embody unwavering expertise, garnered through years of industry mastery. Our team’s extensive knowledge and refined skills ensure effective solutions, fostering trust and delivering excellence.",
    },
    {
      id: 2,
      text: "Innovation",
      selected: false,
      data: "At our core lies a dedication to perpetual innovation. We thrive on pioneering approaches, leveraging cutting-edge technologies, and fostering a culture that encourages imaginative solutions.",
    },
    {
      id: 3,
      text: "Accountability",
      selected: false,
      data: "We hold ourselves responsible for our actions, commitments, and the outcomes we deliver. This unwavering commitment builds trust, transparency, and lasting partnerships with our clients.",
    },
  ];

  function selectButton(id: number) {
    selectedData = buttons.find((button) => button.id === id)?.data || "";
    buttons = buttons.map((button) => ({
      ...button,
      selected: button.id === id,
    }));
  }
</script>

<section class="bg-[#052E26]">
  <div class="grid lg:grid-cols-2 grid-cols-1 p-8 md:p-14 gap-10">
    <div>
      <p class="text-xl bg-[#FFFFFF12] w-fit px-2 py-1 text-white">
        Commitment
      </p>
      <h1
        class="text-5xl font-semibold mt-5 leading-[4.5rem] text-white md:w-5/6"
      >
        Your business goals are our top priority
      </h1>
    </div>
    <div>
      <div class="flex flex-wrap w-full">
        {#each buttons as button}
          <div class="max-md:w-full">
            <button
              class="{button.selected
                ? 'bg-white text-black'
                : 'text-white bg-[#FFFFFF12]'} w-full px-14 py-4 text-lg font-semibold"
              on:click={() => selectButton(button.id)}
            >
              {button.text}
            </button>
          </div>
        {/each}
      </div>
      <div class="mt-10 text-xl text-white">
        <p>{selectedData}</p>
      </div>
    </div>
  </div>
  <div
    class="grid lg:grid-cols-4 md:grid-cols-2 grid-cols-1 p-8 md:p-14 gap-10"
  >
    <div
      class=" bg-[#FFFFFF12] p-8 relative group transition-width z-10 aspect-square flex justify-center items-center"
    >
      <div class=" flex justify-center items-center flex-col gap-5">
        <span
          class="absolute inset-x-0 bottom-0 h-1 bg-[#FFFFFF0D] origin-left transform scale-x-0 transition-transform transition-ease-in-out group-hover:scale-x-100"
        ></span>
        <div class="text-center">
          <Icon icon="wpf:mouse" class="text-white w-24 h-24" />
        </div>
        <div class="text-4xl text-white font-semibold">15 +</div>
        <div class="font-semibold text-lg text-white">
          Years of industry experience
        </div>
      </div>
    </div>
    <div
      class=" bg-[#FFFFFF12] md:p-8 relative group transition-width z-10 aspect-square flex justify-center items-center"
    >
      <div class=" flex justify-center items-center flex-col gap-5">
        <span
          class="absolute inset-x-0 bottom-0 h-1 bg-[#FFFFFF0D] origin-left transform scale-x-0 transition-transform transition-ease-in-out group-hover:scale-x-100"
        ></span>
        <div class="text-center">
          <Icon icon="wpf:mouse" class="text-white w-24 h-24" />
        </div>
        <div class="text-4xl text-white font-semibold">15 +</div>
        <div class="font-semibold text-lg text-white">
          Years of industry experience
        </div>
      </div>
    </div>
    <div
      class=" bg-[#FFFFFF12] p-8 relative group transition-width z-10 aspect-square flex justify-center items-center"
    >
      <div class=" flex justify-center items-center flex-col gap-5">
        <span
          class="absolute inset-x-0 bottom-0 h-1 bg-[#FFFFFF0D] origin-left transform scale-x-0 transition-transform transition-ease-in-out group-hover:scale-x-100"
        ></span>
        <div class="text-center">
          <Icon icon="wpf:mouse" class="text-white w-24 h-24" />
        </div>
        <div class="text-4xl text-white font-semibold">15 +</div>
        <div class="font-semibold text-lg text-white">
          Years of industry experience
        </div>
      </div>
    </div>
    <div
      class=" bg-[#FFFFFF12] p-8 relative group transition-width z-10 aspect-square flex justify-center items-center"
    >
      <div class=" flex justify-center items-center flex-col gap-5">
        <span
          class="absolute inset-x-0 bottom-0 h-1 bg-[#FFFFFF0D] origin-left transform scale-x-0 transition-transform transition-ease-in-out group-hover:scale-x-100"
        ></span>
        <div class="text-center">
          <Icon icon="wpf:mouse" class="text-white w-24 h-24" />
        </div>
        <div class="text-4xl text-white font-semibold">15 +</div>
        <div class="font-semibold text-lg text-white">
          Years of industry experience
        </div>
      </div>
    </div>
  </div>
</section>

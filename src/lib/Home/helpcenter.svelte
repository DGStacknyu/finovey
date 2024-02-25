<script lang="ts">
  import Icon from "@iconify/svelte";
</script>

<section class="grid lg:grid-cols-2 grid-cols-1">
  <div class="py-14 px-8">
    <p class="md:text-xl bg-[#F5F2F0] w-fit px-2 py-1">Help center</p>
    <h1
      class="lg:text-6xl md:text-5xl text-4xl font-semibold mt-5 lg:leading-[4.5rem]"
    >
      Got a question?<br /> Get your answer
    </h1>
    <p class="md:text-xl text-lg mt-5 font-medium">
      Quick answers to questions you may have. Can't find what you're looking
      for? Get in touch with us.
    </p>
    <div class="flex gap-3 mt-6">
      <button
        class="relative overflow-hidden bg-black text-white px-8 py-4 text-lg font-semibold transition-all duration-300 transform-gpu group"
      >
        <span
          class="absolute inset-0 bg-white transform translate-y-full group-hover:translate-y-0 transition-transform duration-300"
        ></span>
        <span class="relative z-10 group-hover:text-black">Get in touch</span>
      </button>
    </div>
  </div>
  <div class="py-14 px-8 space-y-5">
    <div class="collapse collapse-plus bg-[#F5F2F0] p-3 rounded-none">
      <input type="radio" name="my-accordion-3" defaultChecked />
      <div class="collapse-title text-xl font-medium">
        1. How can financial consulting benefit my business?
      </div>
      <div class="collapse-content">
        <hr />
        <p class="mt-6">
          Our consulting optimizes strategies for sustainable growth and
          improved financial performance.
        </p>
      </div>
    </div>
    <div class="collapse collapse-plus bg-[#F5F2F0] p-3 rounded-none">
      <input type="radio" name="my-accordion-3" />
      <div class="collapse-title text-xl font-medium">
        2. What distinguishes your firm from others in the industry?
      </div>
      <div class="collapse-content">
        <hr />
        <p class="mt-6">
          We blend expertise with personalized approaches, focusing on
          client-centric solutions.
        </p>
      </div>
    </div>
    <div class="collapse collapse-plus bg-[#F5F2F0] p-3 rounded-none">
      <input type="radio" name="my-accordion-3" />
      <div class="collapse-title text-xl font-medium">
        3. Do you offer services tailored to specific industries?
      </div>
      <div class="collapse-content">
        <hr />
        <p class="mt-6">
          Yes, our solutions cater to diverse industries, customized to meet
          unique needs.
        </p>
      </div>
    </div>
    <div class="collapse collapse-plus bg-[#F5F2F0] p-3 rounded-none">
      <input type="radio" name="my-accordion-3" />
      <div class="collapse-title text-xl font-medium">
        4. How do you ensure confidentiality with client data?
      </div>
      <div class="collapse-content">
        <hr />
        <p class="mt-6">
          We adhere to strict confidentiality protocols to safeguard all client
          information.
        </p>
      </div>
    </div>
  </div>
</section>

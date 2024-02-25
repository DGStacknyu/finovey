<script lang="ts">
  import { page } from "$app/stores";
  import Icon from "@iconify/svelte";
  import logo from "$lib/images/logo.png";
  const navLinks = [
    { name: "About Us", link: "" },
    { name: "Services", link: "" },
    { name: "Pricing", link: "" },
    { name: "News", link: "" },
    { name: "Contact", link: "" },
  ];
  let isNavOpen = false;
  $: path = $page.url.pathname;

  import { goto } from "$app/navigation";
  const navigateToContactUs = () => {
    goto("/contact-us");
  };
</script>

<header class="text-black bg-white">
  <div class="px-4 py-4 uppercase sm:px-6">
    <div class="flex h-16 items-center justify-between">
      <div class="md:flex md:items-center md:gap-12">
        <a class="block text-teal-600" href="/">
          <span class="sr-only">Home</span>
          <img src={logo} alt="" class="w-40" />
        </a>
        <div class="hidden lg:block">
          <nav aria-label="Global">
            <ul class="flex space-x-8 font-semibold capitalize">
              {#each navLinks as n}
                <!-- Usage -->
                <li
                  class="group transition-width hover:scale-105 relative text-lg"
                >
                  <a href="" class="relative z-10">{n.name}</a>
                  <span
                    class="absolute inset-x-0 bottom-0 h-0.5 bg-black origin-left transform scale-x-0 transition-transform transition-ease-in-out group-hover:scale-x-100"
                  ></span>
                </li>
              {/each}
            </ul>
          </nav>
        </div>
      </div>
      <div class="flex items-center gap-4">
        <div class="flex gap-3 max-md:hidden">
          <button
            class=" border hover:border-black relative overflow-hidden bg-[#F5F2F0] text-black px-8 py-4 text-lg font-semibold transition-all duration-300 transform-gpu group"
          >
            <span
              class="absolute inset-0 bg-white transform translate-y-full group-hover:translate-y-0 transition-transform duration-300"
            ></span>
            <span class="relative z-10 group-hover:text-black"
              >Free consultation</span
            >
          </button>
          <button
            class=" border bg-black relative overflow-hidden text-white px-8 py-4 text-lg font-semibold transition-all duration-300 transform-gpu group"
          >
            <span
              class="absolute inset-0 bg-white transform translate-y-full group-hover:translate-y-0 transition-transform duration-300"
            ></span>
            <span class="relative z-10 group-hover:text-black">Get Started</span
            >
          </button>
        </div>
        <div class="block lg:hidden">
          <button
            on:click={() => (isNavOpen = true)}
            class="rounded p-2 transition"
          >
            <Icon icon="akar-icons:three-line-horizontal" class="h-5 w-5" />
          </button>
        </div>
      </div>
    </div>
  </div>
</header>

<div
  class="{isNavOpen
    ? 'block'
    : 'hidden'} fixed top-0 left-0 w-screen h-screen bg-white opacity-100 z-40 transition-opacity duration-900"
></div>
<nav
  class="fixed top-0 right-0 z-50 w-full md:w-4/6 {isNavOpen
    ? 'translate-y-0'
    : '-translate-y-full'} bg-white p-2 transition-transform duration-300 ease-in-out"
>
  <!-- Navbar content -->

  <div class="flex justify-end pr-1 pt-5">
    <button
      on:click={() => (isNavOpen = false)}
      class="rounded p-2 transition hover:text-gray-600/75"
    >
      <Icon icon="icon-park:close" class="h-5 w-5 " />
    </button>
  </div>
  <div class="p-2">
    <ul class="divide-gray-500 text-base font-medium text-white">
      {#each navLinks as n}
        <li class="py-2">
          <a
            on:click={() => (isNavOpen = false)}
            class="transition text-black px-5 text-xl font-semibold"
            href={n.link}
          >
            {n.name}
          </a>
        </li>
      {/each}
    </ul>
  </div>
</nav>

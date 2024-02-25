<script lang="ts">
  import Icon from "@iconify/svelte";
  import about from "$lib/images/about.png";
  import logo from "$lib/images/logo.png";
</script>

<footer class="relative bg-black mt-60">
  <section class="absolute px-20 -top-1/2">
    <div class="bg-[#F5F2F0] grid lg:grid-cols-2 grid-cols-1">
      <div class="p-14">
        <p class="text-xl bg-white w-fit px-2 py-1">Let's connect</p>
        <h1 class="text-6xl font-semibold mt-5 leading-[4.5rem]">
          We’re here to help
        </h1>
        <p class="text-xl mt-5 font-medium">
          Need help with a project, have a question about our work? We’re here.
        </p>
      </div>
      <div>
        <img src={about} alt="" />
      </div>
    </div>
  </section>
  <div class="mx-auto max-w-screen-xl space-y-8 py-16 lg:space-y-16">
    <div class="grid grid-cols-4 place-content-around p-10 gap-20">
      <div>
        <div class="text-teal-600">
          <img src={logo} alt="" class="object-cover h-8 w-auto" />
        </div>

        <p class="mt-4 max-w-xs text-gray-500">
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Esse non
          cupiditate quae nam molestias.
        </p>
      </div>
      <div>
        <p class="font-medium text-gray-900">Services</p>

        <ul class="mt-6 space-y-4 text-sm">
          <li>
            <a href="#" class="text-gray-700 transition hover:opacity-75">
              Accounts Review
            </a>
          </li>
        </ul>
      </div>
      <div>
        <p class="font-medium text-gray-900">Services</p>

        <ul class="mt-6 space-y-4 text-sm">
          <li>
            <a href="#" class="text-gray-700 transition hover:opacity-75">
              1on1 Coaching
            </a>
          </li>
        </ul>
      </div>
      <ul class="mt-8 flex gap-6">
        <li>
          <a
            href="#"
            rel="noreferrer"
            target="_blank"
            class="text-gray-700 transition hover:opacity-75"
          >
            <span class="sr-only">Facebook</span>
            <Icon icon="ri:facebook-fill" />
          </a>
        </li>
        <li>
          <a
            href="#"
            rel="noreferrer"
            target="_blank"
            class="text-gray-700 transition hover:opacity-75"
          >
            <span class="sr-only">Instagram</span>
            <Icon icon="ri:instagram-line" />
          </a>
        </li>

        <li>
          <a
            href="#"
            rel="noreferrer"
            target="_blank"
            class="text-gray-700 transition hover:opacity-75"
          >
            <span class="sr-only">Twitter</span>
            <Icon icon="mdi:twitter" />
          </a>
        </li>
      </ul>
    </div>
  </div>
</footer>

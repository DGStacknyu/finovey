<script>
  import Icon from "@iconify/svelte";
  import user from "$lib/images/user.png";
</script>

<div class="bg-white relative overflow-hidden space-y-5 md:px-6 px-4 py-10">
  <h2 class="font-semibold md:text-2xl text-xl">
    Helped navigate regulatory challenges. Valued advisors for strategic
    financial decisions.
  </h2>
  <div class="flex items-center gap-5 mt-3">
    <img src={user} class="rounded-full w-20 h-20 object-cover" />
    <div>
      <p class="text-xl font-semibold">Frederic Hill</p>
      <p class="font-base">Founder & CEO</p>
    </div>
  </div>
  <hr />
  <p class="text-4xl font-semibold">+120 %</p>
  <p class="text-base md:text-lg capitalize">
    Increase in customer growth rate
  </p>
</div>

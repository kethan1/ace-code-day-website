<template>
  <div class="w-full h-14 px-3 bg-[#164d46] shadow">
    <div class="max-w-[65ch] lg:max-w-[80ch] xl:max-w-[100ch] mx-auto h-full flex items-center justify-between">
      <div>
        <a class="px-2 py-1 rounded transition-shadow text-white text-2xl font-semibold hover:shadow-[0px_0px_15px_rgba(0,0,0,0.25)]" href="#home">
          ACE <code class="bg-[#27c940]/20 border border-[#27c940]/40 rounded px-1 font-normal">Code</code> Day
        </a>
      </div>
      <button class="md:hidden text-white">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
      </button>
      <div class="hidden md:inline-flex items-center space-x-2">
        <div
          v-for="(link, index) in links"
          :key="`link-${index}`"
        >
          <a class="p-2 rounded transition-shadow hover:shadow-[0px_0px_15px_rgba(0,0,0,0.25)] text-white text-lg font-semibold" :href="link.href">
            {{ link.title }}
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          title: "About",
          href: "#about",
        },
        {
          title: "Schedule",
          href: "#schedule",
        },
        {
          title: "Workshops",
          href: "#workshops",
        },
        {
          title: "Sign Up",
          href: "#sign-up",
        },
      ],
    };
  },
};
</script>

<style>
</style>

<template>
  <div class="lg:flex lg:space-x-8 lg:items-center">
    <div class="lg:flex-1 lg:prose-h2:mt-0 lg:prose-p:mb-0">
      <slot />
    </div>
    <div class="not-prose flex flex-col p-3 border-2 border-[#27c940]/25 rounded-md bg-[#27c940]/10 h-52 sm:h-72 w-full lg:flex-1 mx-auto">
      <img class="rounded min-h-0 flex-1 object-cover shadow-md" :src="require(`../assets/${src}`)" :alt="alt">
      <p class="mt-3 italic text-sm">
        {{ alt }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    src: {
      required: true,
      type: String,
    },
    alt: {
      required: true,
      type: String,
    },
  },
};
</script>

<style>

</style>

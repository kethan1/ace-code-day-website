<template>
  <div class="px-5 border-2 border-[#27c940]/25 rounded-md bg-gradient-to-br from-[#27c940]/10 to-[#27c940]/0 shadow-md">
    <ol class="relative border-l border-[#1d6529] py-3 list-none">
      <h2 class="my-3 sm:my-3">
        {{ title }}
      </h2>
      <li
        v-for="(event, index) in data"
        :key="`event-${index}`"
        class="mb-4 lg:mb-6 ml-2 not-prose"
      >
        <div class="absolute w-4 h-4 rounded-full mt-2 -left-2 border-2 border-[#7ed68b] bg-[#4b8153]" />
        <time class="text-sm lg:text-base font-light leading-none text-slate-300">
          {{ event.time }}
        </time>
        <h3
          class="text-lg lg:text-xl mt-1 font-semibold text-white"
          :class="{
            'mb-2 lg:mb-4': (event.description === undefined),
          }"
        >
          {{ event.title }}
        </h3>
        <p v-if="event.description !== undefined" class="mt-1 mb-2 lg:mb-4 text-sm lg:text-base font-normal text-slate-300">
          {{ event.description }}
        </p>
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      required: true,
      type: String,
    },
    data: {
      required: true,
      type: Array,
    },
  },
};
</script>

<style>

</style>

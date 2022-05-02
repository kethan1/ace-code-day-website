<template>
  <div>
    <Hero />
    <div class="bg-slate-900 px-6 py-8 sm:py-14">
      <nuxt-content class="lg:max-w-[80ch] xl:max-w-[100ch] mx-auto prose prose-sm sm:prose-base prose-invert" :document="about" />
    </div>
    <div class=" bg-gradient-to-br from-[#16474d] to-[#22213f] px-6 py-8 sm:py-14">
      <nuxt-content class="lg:max-w-[80ch] xl:max-w-[100ch] mx-auto prose prose-sm sm:prose-base prose-invert" :document="schedule" />
    </div>
    <div class="bg-slate-900 px-6 py-8 sm:py-14">
      <nuxt-content class="lg:max-w-[80ch] xl:max-w-[100ch] mx-auto prose prose-sm sm:prose-base prose-invert" :document="workshops" />
      <Workshops class="max-w-[65ch] lg:max-w-[80ch] xl:max-w-[100ch] mx-auto" :data="workshopsData.workshops" />
    </div>
    <div class=" bg-gradient-to-br from-[#16474d] to-[#22213f] px-6 py-8 sm:py-14">
      <nuxt-content class="lg:max-w-[80ch] xl:max-w-[100ch] mx-auto prose prose-sm sm:prose-base prose-invert" :document="signUp" />
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const about = await $content("about").fetch();
    const schedule = await $content("schedule").fetch();
    const workshops = await $content("workshops").fetch();
    const workshopsData = await $content("workshops-data").fetch();
    const signUp = await $content("sign-up").fetch();
    return {
      about,
      schedule,
      workshops,
      workshopsData,
      signUp,
    };
  },
};
</script>

<style>
</style>

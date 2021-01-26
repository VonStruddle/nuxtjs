<template>
  <div>
    <h1 class="text-4xl">{{ page.title }}</h1>
    <nuxt-content :document="page" />
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const page = await $content("hello").fetch();
    return { page };
  },
};
</script>

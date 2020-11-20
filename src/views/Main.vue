<template>
  <div class="main">
    <banner></banner>
    <about-me></about-me>
    <feature></feature>
    <parallax></parallax>
    <blog></blog>
    <contact-me></contact-me>
  </div>
</template>

<script>
export default {
  name: "Main",
  components: {
    Banner: () => import("@/components/main/Banner.vue"),
    AboutMe: () => import("@/components/main/AboutMe.vue"),
    Feature: () => import("@/components/main/Feature.vue"),
    Parallax: () => import("@/components/main/Parallax.vue"),
    Blog: () => import("@/components/main/Blog.vue"),
    ContactMe: () => import("@/components/main/ContactMe.vue")
  }
};
</script>

<style lang="scss" scoped>
.main {
  padding-bottom: 60px;
}
</style>
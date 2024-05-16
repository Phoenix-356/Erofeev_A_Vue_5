<template>
  <div id="app">
    <HomePage></HomePage>

    <!-- <BlogPage></BlogPage>

    <BlogDetailsPage></BlogDetailsPage> -->
  </div>
</template>

<script>
import HomePage from "./pages/HomePage.vue";

// import BlogPage from "./pages/BlogPage.vue";

// import BlogDetailsPage from "./pages/BlogDetailsPage.vue";

export default {
  name: "App",
  components: {
    HomePage,
    // BlogPage,
    // BlogDetailsPage,
  },
};
</script>

<style lang="scss">
@import "scss/vars";
.center {
  padding-left: calc(50% - 1200px / 2);
  padding-right: calc(50% - 1200px / 2);
}

* {
  margin: 0;
  padding: 0;
}

a {
  text-decoration: none;
}
</style>

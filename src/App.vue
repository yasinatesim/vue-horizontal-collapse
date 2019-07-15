<template>
  <div id="app">
    <GithubCorner />
    <HorizontalCollapse />
  </div>
</template>

<script>
import HorizontalCollapse from "./components/HorizontalCollapse";
import GithubCorner from "./components/GithubCorner";

export default {
  name: "app",
  components: {
    HorizontalCollapse,
    GithubCorner
  }
};
</script>

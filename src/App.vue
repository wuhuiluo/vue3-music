<template>
  <Father />
  <m-header />
  <tab />
  <router-view />
</template>
<script>
import Father from "@/components/father";
import MHeader from "@/components/header/header";
import Tab from "@/components/tab/tab";

export default {
  components: {
    MHeader,
    Tab,
    Father,
  },
};
</script>
<style lang="scss">
</style>

<template>
  <div class="search"></div>
</template>


<script>
import { getRecommend } from "../api/recommend";
export default {
  name: "recommend",
  async created() {
    const data = await getRecommend();
    console.log(data);
  },
};
</script>


<style>
</style>

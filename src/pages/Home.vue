<template>
  <h1 class="title">Welcome to the Forum</h1>
  <thread-list :threads="threads" />
</template>

<script>
import db from "@/data.json";
import ThreadList from "@/components/thread/ThreadList.vue";

export default {
  name: "Home",
  components: {
    ThreadList,
  },
  data() {
    return {
      threads: db.threads,
    };
  },
};
</script>

<style scoped>
.title {
  color: #223250;
  text-align: center;
}
</style>

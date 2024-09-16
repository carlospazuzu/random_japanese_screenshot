<template>
  <div class="container">
    <Suspense>
      <ContentEntity />
    </Suspense>
  </div>
</template>

<script>
import ContentEntity from "./components/ContentEntity.vue";

export default {
  components: {
    ContentEntity,
  },
};
</script>

<style>
body {
  background-color: #111;
}

.centered {
  text-align: center;
}
</style>

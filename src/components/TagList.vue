<template>
  <GrammarTag v-for="(tag, index) in tags" :key="index" :tag="tag" />
</template>

<script>
import GrammarTag from "./GrammarTag.vue";

export default {
  props: ["tags"],
  components: { GrammarTag },
};
</script>

<style scope></style>

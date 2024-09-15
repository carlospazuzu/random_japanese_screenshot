<template>
  <span>#{{ tag }}</span>
</template>

<script>
export default {
  props: ["tag"],
};
</script>

<style scoped>
span {
  background-color: #ef4037;
  color: #eee;
  padding: 6px;
  border-radius: 4px;
  margin: 40px 12px 0px 0px;
}
</style>

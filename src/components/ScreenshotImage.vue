<template>
  <div>
    <img
      :src="require(`@/assets/screenshots/${this.image}.png`)"
      height="400px"
    />
  </div>
</template>

<script>
export default {
  props: ["image"],
};
</script>

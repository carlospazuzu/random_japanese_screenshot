<template>
  <div>
    <img
      :src="`https://japanesestudies.github.io/randomss_data/screenshots/${this.image}.png`"
      height="400px"
    />
  </div>
</template>

<script>
export default {
  props: ["image"],
};
</script>

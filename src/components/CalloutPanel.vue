<template>
  <div class="callout-jp">
    <h6>{{ title }}</h6>
    <span>{{ content }}</span>
  </div>
  <div class="callout-pt">
    <h6>Tradução</h6>
    <span>{{ translation }}</span>
  </div>
</template>

<script>
export default {
  props: ["title", "content", "translation", "vocabulary"],
};
</script>

<style scoped>
.callout-jp {
  border-radius: 4px;
  background-color: #11224d;
  color: #5b84c4;
  padding: 16px;
  margin: 16px 0px;
}

.callout-pt {
  border-radius: 4px;
  background-color: #f98125;
  color: #fdd4b5;
  padding: 16px;
  margin: 4px 0px;
}

h6 {
  font-weight: bold;
}

span {
  font-size: 18px;
}
</style>

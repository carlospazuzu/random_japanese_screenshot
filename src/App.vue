<template>
  <div class="container">
    <div class="centered">
      <ScreenshotImage :image="randomData.image" />
    </div>
    <CalloutPanel
      :title="randomData.title"
      :content="randomData.text"
      :translation="randomData.translation"
    />
    <br />
    <TagList :tags="randomData.tags" />
  </div>
</template>

<script>
import data from "./data/data.json";
import { ref } from "vue";
import CalloutPanel from "./components/CalloutPanel.vue";
import ScreenshotImage from "./components/ScreenshotImage.vue";
import TagList from "./components/TagList.vue";

export default {
  components: {
    CalloutPanel,
    ScreenshotImage,
    TagList,
  },
  setup() {
    let randomPosition = parseInt(Math.random() * data.size);
    let randomData = ref(data.data[randomPosition]);

    return { randomData };
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

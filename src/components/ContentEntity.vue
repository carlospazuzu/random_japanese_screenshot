<template>
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
</template>

<script>
import { ref } from "vue";

import CalloutPanel from "./CalloutPanel.vue";
import ScreenshotImage from "./ScreenshotImage.vue";
import TagList from "./TagList.vue";

const data = ref();

export default {
  components: {
    ScreenshotImage,
    CalloutPanel,
    TagList,
  },
  async setup() {
    const response = await fetch(
      "https://japanesestudies.github.io/randomss_data/data.json"
    );
    data.value = await response.json();

    const randomPosition = parseInt(Math.random() * data.value.size);
    const randomData = data.value.data[randomPosition];

    return { randomData };
  },
};
</script>

<style scoped>
.centered {
  text-align: center;
}
</style>

<template>
  <table class="u-full-width">
    <thead>
      <tr>
        <th>Palavra</th>
        <th>Leitura</th>
        <th>Tradução</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(word, index) in vocabulary" :key="index">
        <td>{{ word.word }}</td>
        <td>{{ word.reading }}</td>
        <td>{{ word.meaning }}</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  props: ["vocabulary"],
};
</script>

<style scoped>
table {
  color: white;
}
</style>

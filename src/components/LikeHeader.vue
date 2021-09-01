<template>
  <div>
    <slot>slot経由のデータがない場合に表示される(フォールバックコンテンツ)</slot>
    <p>{{ headerText }}</p>
  </div>
</template>

<script>
export default {
  props: ["headerText"]
}
</script>

<style scoped>
/* 子要素と同じ要素にスタイルを適用させた場合は、親のスタイルが適用される */
h1 {
  color: blue;
}
</style>
<template>
  <div id="app">
    <LikeHeader data-from-parent="props経由の親からのstring(受け渡し側:ケバブケース)">
      <h1>slot経由のHTML</h1>
      <h2>{{ parentData }}</h2>
    </LikeHeader>
  </div>
</template>

<script>
import LikeHeader from './components/LikeHeader'

export default {
  data() {
    return {
      parentData: '親のdataです'
    };
  },
  components: {
    LikeHeader
  }
}
</script>

<style>
/* 子要素と同じ要素にスタイルを適用させた場合は、親のスタイルが適用される */
h1 {
  color: red;
}
</style>

<template>
  <div id="app">
    <LikeHeader header-text="props経由の親からのstring">
      <!-- <h1>slot経由のHTML</h1>
      <h2>{{ number }}</h2> -->
    </LikeHeader>
  </div>
</template>

<script>
import LikeHeader from './components/LikeHeader'

export default {
  data() {
    return {
      number: 14
    };
  },
  props: ["headerText"],
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

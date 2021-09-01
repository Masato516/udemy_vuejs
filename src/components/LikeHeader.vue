<template>
  <div>
    <slot>slot経由のデータがない場合に表示される(フォールバックコンテンツ)</slot>
    <p>{{ dataFromParent }} (受け取り側はキャメルケース)</p>
    <p>{{ upperCaseData1 }}: computed経由</p>
    <p>{{ upperCaseData2 }}: computed経由2(computedだと冗長になる！！！)</p>
    <p>{{ rawData1 | upperCase }}: filter経由</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      rawData1: "raw data(1)",
      rawData2: "raw data(2)"
    }
  },
  computed: {
    upperCaseData1() { // 引数を渡せない！！
      return this.rawData1.toUpperCase();
    },
    upperCaseData2() {
      return this.rawData2.toUpperCase();
    }
  },
  props: ["dataFromParent"]
}
</script>

<style scoped>
/* 子要素と同じ要素にスタイルを適用させた場合は、親のスタイルが適用される */
h1 {
  color: blue;
}
</style>
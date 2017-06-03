<template>
  <div>
    <slot></slot>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="css">
.label {
    fill: black;
  }
  .bottle, .wine-text {
    fill: white;
  }
  .flor {
    fill: #ccc;
  }
  .bkimg {
    filter:url(#inverse)
  }
</style>

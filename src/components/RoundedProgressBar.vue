<template>
  <div class="progress-bar">
    <div
      class="progress"
      :style="{ width: progress + '%' }"
      :title="`热度: ${progress}`"
    ></div>
  </div>
</template>

<script>
export default {
  name: 'RoundedProgressBar',
  props: {
    progress: {
      type: Number,
      required: true,
      validator: value => value >= 0 && value <= 100,
    },
  },
};
</script>

<style scoped>
.progress-bar {
  width: 90px;
  height: 7px;
  background-color: #e0e0e0;
  border-radius: 5px;
  border: 1px solid #7a7a7a70;
  overflow: hidden;
  opacity: 0.5;
}

.progress {
  height: 100%;
  background-color: #7a7a7a;
  border-radius: 2px;
}
</style>

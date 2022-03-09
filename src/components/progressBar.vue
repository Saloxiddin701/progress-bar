<template>
  <div class="progress-bar">
    <div :class="(progress === 100) ? 'progress-inner complete' : 'progress-inner'"
         :style="`width: ${progress}%`">
      <span :class="(progress > 50) ? 'white' : ''">{{ progress }}%</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "progressBar",
  props: ['progress']
}
</script>

<style>
  .progress-bar {
    width: 100%;
    height: 20px;
    background: #ffffff;
    position: relative;
  }
  .progress-inner {
    height: 100%;
    background: linear-gradient(to right, #ed008d, #2484e4);
    border-radius: 0 10px 10px 0;
  }
  .progress-inner span {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: #313131;
    font-size: 14px;
  }
  .progress-inner.complete {
    border-radius: 0;
  }
  .progress-inner span.white {
    color: #ffffff;
  }
</style>
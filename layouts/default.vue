<template>
  <div class="slidev-layout default">
    <div class="watermark"></div>
    <slot />
  </div>
</template>

<style scoped>
.slidev-layout.default {
  position: relative;
}

.watermark {
  position: absolute;
  inset: 0;
  background-image: url('/paf_clean_circle.png');
  background-repeat: no-repeat;
  background-position: right 6% center;
  background-size: 34%;
  opacity: 0.045;
  filter: grayscale(100%) contrast(90%);
  pointer-events: none;
}

.slidev-layout.default > *:not(.watermark) {
  position: relative;
  z-index: 1;
}
</style>

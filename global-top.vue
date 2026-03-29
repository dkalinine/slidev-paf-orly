<script setup>
import { useSlideContext } from '@slidev/client'
const { $page } = useSlideContext()
</script>

<template>
  <div class="global-header">
    <img src="/logo-ministere-interieur.png" alt="Ministère de l'Intérieur" />
    <img src="/logo-paf.png" alt="PAF" />
  </div>
</template>

<style>
.global-header {
  position: absolute;
  top: 14px;
  right: 24px;
  display: flex;
  align-items: center;
  gap: 12px;
  z-index: 20;
}
.global-header img:first-child {
  height: 40px;
}
.global-header img:last-child {
  height: 34px;
}
</style>

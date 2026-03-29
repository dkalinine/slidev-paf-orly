<script setup>
import { useSlideContext } from '@slidev/client'
const { $page } = useSlideContext()
</script>

<template>
  <div :class="$page === 1 ? 'global-header-hero' : 'global-header'">
    <img src="/logo-ministere-interieur.png" alt="Ministère de l'Intérieur" />
    <img src="/logo-paf.png" alt="PAF" />
  </div>
</template>

<style>
/* En-tête discret sur les slides 2+ */
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

/* Logos plus grands sur la slide d'accueil */
.global-header-hero {
  position: absolute;
  top: 28px;
  left: 36px;
  display: flex;
  align-items: center;
  gap: 20px;
  z-index: 20;
}
.global-header-hero img:first-child {
  height: 80px;
}
.global-header-hero img:last-child {
  height: 68px;
}
</style>

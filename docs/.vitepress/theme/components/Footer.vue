<script setup lang="ts">
import { useLayout } from 'vitepress/theme';

const { hasSidebar } = useLayout();
</script>

<template>
  <footer class="VPFooter" :class="{ 'has-sidebar': hasSidebar }">
    <div class="container">
      <p>
        镜像自 <a href="https://survive-hfut.cc" target="_blank">survive-hfut.cc</a>
      </p>
      <p>
        <a href="https://beian.miit.gov.cn/" target="_blank">黑ICP备2023010514号</a>
      </p>
    </div>
  </footer>
</template>

<style scoped>
/**
    https://github.com/vuejs/vitepress/blob/main/src/client/theme-default/components/VPFooter.vue
*/

.VPFooter {
  position: relative;
  z-index: var(--vp-z-index-footer);
  border-top: 1px solid var(--vp-c-gutter);
  padding: 32px 24px;
  background-color: var(--vp-c-bg);
}

.VPFooter.has-sidebar {
  display: none;
}

.VPFooter :deep(a) {
  text-decoration-line: underline;
  text-underline-offset: 2px;
  transition: color 0.25s;
}

.VPFooter :deep(a:hover) {
  color: var(--vp-c-text-1);
}

@media (min-width: 768px) {
  .VPFooter {
    padding: 32px;
  }
}

.container {
  margin: 0 auto;
  max-width: var(--vp-layout-max-width);
  text-align: center;
}

.container > * {
  line-height: 24px;
  font-size: 14px;
  font-weight: 500;
  color: var(--vp-c-text-2);
}
</style>

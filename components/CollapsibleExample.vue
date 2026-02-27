<template>
  <details class="collapsible-example">
    <summary class="collapsible-example__summary">{{ summary }}</summary>
    <div class="collapsible-example__content">
      <slot />
    </div>
  </details>
</template>

<script setup lang="ts">
defineProps<{
  /** 접었을 때 보이는 한 줄 요약 (클릭 시 펼침) */
  summary: string
}>()
</script>

<style scoped>
.collapsible-example {
  margin: 0.5rem 0 0.75rem 0;
  border: 1px solid color-mix(in srgb, var(--page-primary) 25%, transparent);
  border-radius: 6px;
  background: color-mix(in srgb, var(--page-primary) 4%, var(--page-background));
}

.collapsible-example__summary {
  padding: 0.5rem 0.75rem;
  font-size: 0.85em;
  font-weight: 600;
  color: var(--page-primary);
  cursor: pointer;
  list-style: none;
  user-select: none;
}

.collapsible-example__summary::-webkit-details-marker {
  display: none;
}

.collapsible-example__summary::before {
  content: '▶ ';
  display: inline-block;
  margin-right: 0.25rem;
  font-size: 0.7em;
  transition: transform 0.2s ease;
}

.collapsible-example[open] .collapsible-example__summary::before {
  transform: rotate(90deg);
}

.collapsible-example__content {
  padding: 0 0.75rem 0.75rem;
  border-top: 1px solid color-mix(in srgb, var(--page-primary) 12%, transparent);
}

.collapsible-example__content :deep(pre),
.collapsible-example__content :deep(.shiki) {
  margin: 0.5rem 0 0;
  padding: 0.75rem;
  font-size: 0.55em;
  line-height: 1.4;
  overflow-x: auto;
  border-radius: 4px;
  background: color-mix(in srgb, var(--page-color) 6%, var(--page-background));
}

.collapsible-example__content :deep(p) {
  margin: 0.5rem 0 0;
  font-size: 0.75em;
  color: var(--page-muted);
}
</style>

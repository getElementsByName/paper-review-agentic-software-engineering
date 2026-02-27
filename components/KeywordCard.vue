<template>
  <div class="keyword-card">
    <div class="keyword-card__main">{{ keyword }}</div>
    <div class="keyword-card__sub">{{ subtitle }}</div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  /** 한글 키워드(주제명) */
  keyword: string
  /** 영문 풀네임 및 약어, 예: "Structured Agentic Software Engineering, SASE" */
  subtitle: string
}>()
</script>

<style scoped>
.keyword-card {
  display: inline-block;
  padding: 0.75rem 1.25rem;
  border-radius: 0.5rem;
  border: 1px solid color-mix(in srgb, var(--page-color) 12%, transparent);
  background: linear-gradient(to bottom, var(--page-background), color-mix(in srgb, var(--page-color) 6%, var(--page-background)));
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);
}

.keyword-card__main {
  font-weight: 700;
  font-size: 1.05em;
  color: var(--page-color);
  line-height: 1.35;
}

.keyword-card__sub {
  margin-top: 0.25rem;
  font-size: 0.9em;
  color: var(--page-muted);
  font-style: italic;
}
</style>

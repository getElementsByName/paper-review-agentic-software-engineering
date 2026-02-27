<template>
  <div class="source-note">참고: {{ text }}</div>
</template>

<script setup lang="ts">
defineProps<{
  /** "참고:" 뒤에 올 출처/해석 내용 (예: 출처(원문): §9) */
  text: string
}>()
</script>

<style scoped>
.source-note {
  margin-top: 0.75rem;
  font-size: 0.65em;
  color: var(--page-muted);
  line-height: 1.4;
}
</style>

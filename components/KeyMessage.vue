<template>
  <div class="key-message">
    <div v-if="label" class="key-message__label">{{ label }} </div>
    <div class="key-message__text">{{ message }}</div>
  </div>
</template>

<script setup lang="ts">
withDefaults(
  defineProps<{
    /** 이 슬라이드에서 전달하는 한 문장 핵심 메시지·인사이트 */
    message: string
    /** 접두 레이블 (비우면 레이블 없이 메시지만 표시) */
    label?: string
  }>(),
  { label: 'Key Message' }
)
</script>

<style scoped>
.key-message {
  display: block;
  margin: 0.5rem 0 0.75rem 0;
  padding: 0.5rem 0 0.5rem 0.75rem;
  border-left: 3px solid var(--page-primary);
  background: color-mix(in srgb, var(--page-primary) 6%, transparent);
  border-radius: 0 4px 4px 0;
  line-height: 1.4;
}

.key-message__label {
  font-size: 0.56em;
  font-weight: 600;
  color: var(--page-primary);
}

.key-message__text {
  font-weight: 600;
  font-size: 0.95em;
  color: var(--page-color);
}
</style>

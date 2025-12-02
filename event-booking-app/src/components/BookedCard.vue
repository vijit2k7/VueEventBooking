<template>
  <SectionCard>
    <template #header>
      <div class="flex items-center justify-between gap-3">
        <p class="title">
          {{ event.title }}
        </p>
        <span
          class="inline-flex items-center gap-1 rounded-full border border-emerald-200 bg-emerald-50 px-3 py-1 text-[11px] font-semibold uppercase tracking-[0.18em] text-emerald-600"
        >
          <span class="h-1.5 w-1.5 rounded-full bg-emerald-500"></span>
          Booked
        </span>
      </div>
    </template>
  </SectionCard>
</template>

<script setup>
import { defineProps } from 'vue';
import SectionCard from './SectionCard.vue';

defineProps({
  event: {
    type: Object,
    required: true
  }
});
</script>

<style scoped>
@reference "../assets/main.css";

.title {
  @apply text-sm md:text-base font-medium text-slate-900;
}
</style>

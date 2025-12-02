<template>
  <SectionCard>
    <template #header>
      <div class="flex items-start justify-between gap-3">
        <h2 class="title">{{ event.title }}</h2>
        <span
          class="inline-flex items-center rounded-full bg-emerald-50 border border-emerald-200 px-3 py-1 text-[11px] font-medium text-emerald-600"
        >
          <span class="mr-1.5 inline-block h-1.5 w-1.5 rounded-full bg-emerald-500 animate-pulse" />
          Upcoming
        </span>
      </div>
    </template>

    <p class="when flex items-center gap-2 text-xs uppercase tracking-[0.15em] text-emerald-500/80">
      <span class="inline-block h-[1px] w-7 bg-emerald-400/80"></span>
      {{ event.date }}
      <span class="inline-block h-[1px] flex-1 bg-slate-200"></span>
    </p>

    <template #footer>
      <p class="description text-sm text-slate-600">
        {{ event.description }}
      </p>
      <Button @click="$emit('register')">
        Register
      </Button>
    </template>
  </SectionCard>
</template>

<script setup>
import { defineProps } from 'vue';
import Button from './Button.vue';
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
  @apply text-base md:text-lg font-semibold text-slate-900;
}

.when {
  @apply mt-1 mb-2;
}

.description {
  @apply max-w-xs md:max-w-sm;
}
</style>

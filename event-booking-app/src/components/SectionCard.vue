<template>
  <RoundedCard>
    <div class="flex flex-col gap-3">
      <h2 v-if="$slots.header" class="text-lg md:text-xl font-semibold tracking-tight text-slate-900">
        <slot name="header"></slot>
      </h2>

      <div v-if="$slots.default" class="text-sm md:text-base text-slate-600">
        <slot></slot>
      </div>

      <div
        v-if="$slots.footer"
        class="mt-2 pt-3 border-t border-slate-200 flex flex-wrap items-center justify-between gap-3 text-slate-500"
      >
        <slot name="footer"></slot>
      </div>
    </div>
  </RoundedCard>
</template>

<script setup>
import RoundedCard from './RoundedCard.vue';
</script>
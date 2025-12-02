<template>
  <button
    class="inline-flex items-center justify-center gap-2 rounded-full px-5 py-2.5 mt-2
           text-sm font-medium tracking-wide
           bg-emerald-500 text-white
           shadow-[0_12px_30px_rgba(16,185,129,0.35)]
           hover:bg-emerald-400 hover:shadow-[0_16px_38px_rgba(16,185,129,0.45)]
           focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-emerald-400 focus-visible:ring-offset-2 focus-visible:ring-offset-white
           active:scale-[0.97] active:bg-emerald-500
           transition-all duration-200 ease-out"
    @click="$emit('click')"
  >
    <span class="h-1.5 w-1.5 rounded-full bg-white/70"></span>
    <slot></slot>
  </button>
</template>

<script setup>
import { defineEmits } from 'vue';

defineEmits(['click']);
</script>
<template>
  <div
    class="event-card relative overflow-hidden rounded-2xl border border-slate-200 bg-white
           shadow-[0_15px_45px_rgba(15,23,42,0.08)] hover:shadow-[0_20px_55px_rgba(15,23,42,0.12)]
           transition-all duration-300 ease-out transform hover:-translate-y-1 hover:border-emerald-300"
  >
    <div
      class="pointer-events-none absolute inset-0 opacity-0 hover:opacity-100 transition-opacity duration-500"
    >
      <div
        class="absolute -top-20 -right-24 h-48 w-48 rounded-full bg-emerald-400/20 blur-3xl"
      ></div>
    </div>
    <div class="relative p-5 md:p-6">
      <slot></slot>
    </div>
  </div>
</template>

<script setup>
</script>
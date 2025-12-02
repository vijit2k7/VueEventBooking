<script setup>
import EventList from './components/EventList.vue';
</script>

<template>
  <div
    class="min-h-screen bg-gradient-to-br from-slate-50 via-white to-emerald-50 text-slate-900 flex items-center justify-center px-4 py-10"
  >
    <div
      class="w-full max-w-6xl bg-white/90 backdrop-blur-sm rounded-3xl border border-slate-200 shadow-[0_25px_80px_rgba(148,163,184,0.25)] px-6 py-8 md:px-10 md:py-10"
    >
      <div class="flex flex-col md:flex-row md:items-center md:justify-between gap-4 mb-8">
        <div>
          <p class="text-xs uppercase tracking-[0.35em] text-emerald-500/80 mb-2">
            Plan your next experience
          </p>
          <h1 class="text-3xl md:text-4xl font-semibold tracking-tight text-slate-900">
            Event Booking
            <span class="text-emerald-500">Dashboard</span>
          </h1>
          <p class="mt-2 text-sm md:text-base text-slate-600 max-w-xl">
            Browse upcoming events, register with a single click, and keep track of the ones
            you’ve already booked.
          </p>
        </div>
        <div class="flex items-center gap-3 text-xs md:text-sm text-slate-500">
          <span class="inline-flex h-2 w-2 rounded-full bg-emerald-500 animate-pulse"></span>
          <span>Real-time booking preview</span>
        </div>
      </div>

      <EventList />
    </div>
  </div>
</template>

<style scoped></style>

<template>
  <div class="space-y-10">
    <div>
      <div class="flex items-center justify-between mb-4">
        <h2 class="text-lg md:text-xl font-semibold tracking-tight text-slate-900">
          Upcoming events
        </h2>
        <p class="text-xs text-slate-500">
          Click
          <span class="font-semibold text-emerald-500">Register</span>
          to add an event to your booked list
        </p>
      </div>

      <div
        class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-5 md:gap-6 items-stretch"
      >
        <EventCard
          v-for="event in events"
          :key="event.id"
          :event="event"
          @register="childEvent(event)"
        />
      </div>
    </div>

    <div class="booked-events">
      <div class="flex items-center justify-between mb-4">
        <h2 class="text-lg md:text-xl font-semibold tracking-tight text-slate-900">
          Booked events
        </h2>
        <span
          class="inline-flex items-center gap-2 rounded-full bg-slate-100 px-3 py-1 text-xs text-slate-600 border border-slate-200"
        >
          <span class="inline-flex h-1.5 w-1.5 rounded-full bg-emerald-500"></span>
          {{ bookedEvents.length }} booked
        </span>
      </div>
      <div
        v-if="bookedEvents.length"
        class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 md:gap-5"
      >
        <BookedCard
          v-for="event in bookedEvents"
          :key="event.id"
          :event="event"
        />
      </div>
      <p v-else class="text-sm text-slate-500 italic">
        You haven’t booked any events yet. Start by registering for one above.
      </p>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import BookedCard from './BookedCard.vue';
import EventCard from './EventCard.vue';

let events = [
  { id: 1, title: 'Vue.js Conference', date: '2024-09-15', description: 'New York' },
  { id: 2, title: 'JavaScript Summit', date: '2024-10-20', description: 'San Francisco' },
  { id: 3, title: 'Web Dev Meetup', date: '2024-11-05', description: 'Chicago' },
  { id: 4, title: 'Vue.js2 Conference', date: '2024-09-15', description: 'New York' },
  { id: 5, title: 'JavaScript2 Summit', date: '2024-10-20', description: 'San Francisco' },
  { id: 6, title: 'Web Dev2 Meetup', date: '2024-11-05', description: 'Chicago' },
];

const bookedEvents = ref([
  { id: 1, title: 'Vue.js Conference', date: '2024-09-15', description: 'New York' },
  { id: 3, title: 'Web Dev Meetup', date: '2024-11-05', description: 'Chicago' },
]);

function childEvent(event) {
  const exists = bookedEvents.value.some((e) => e.id === event.id);
  if (!exists) {
    bookedEvents.value.push(event);
  }
}
</script>

<style scoped></style>

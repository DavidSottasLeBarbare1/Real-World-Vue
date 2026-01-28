<script setup>
import EventCard from '@/components/EventCard.vue'
import { ref } from 'vue'

const events = ref([
  {
    id: 5928101,
    category: 'Petrouchka adoption center',
    title: 'Pepet Adoption Day',
    description: 'Adopt Pepet today',
    location: 'Préverenges',
    date: 'January 28, 2026',
    time: '12:00',
    petsAllowed: true,
    organizer: 'Latif Krasniqi',
  },
  {
    id: 4582797,
    category: 'Politic',
    title: "Senan's ceremony",
    description: 'Senan becomes the 45th president of sri lanka',
    location: 'Colombo',
    date: 'March 14, 1760',
    time: '10:00',
    petsAllowed: true,
    organizer: 'Senan Gnanassorian',
  },
  {
    id: 8419988,
    category: 'Surprise',
    title: 'MrBeast in ETML',
    description:
      'The youtuber Mr Beast is coming over to the ETML to greet the make-a-wish kid named Albert',
    location: 'Lausanne',
    date: 'February 30, 2026',
    time: '11:00',
    petsAllowed: false,
    organizer: 'Bertrand Sahli',
  },
])
</script>

<template>
  <h1>Superb events !</h1>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>
<style>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>

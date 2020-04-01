<template>
  <div>
    <h1>Events Listing</h1>
    <EventCard title="Park Cleanup"/>
    <EventCard title="Room Tidy up"/>
  </div>
</template>

<script>
import EventCard from '@/components/EventCard.vue'

export default {
  components: {
    EventCard
  }
}
</script>

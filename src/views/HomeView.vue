<template>
   <h1>Events For Good</h1>
  <div class="events">
    <img alt="Vue logo" src="../assets/logo.png" />
    <EventCard v-for="event in events" :key="event.id" :event="event"/>
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";

export default {
  name: "HomeView",
  components: {
    EventCard,
  },
  data(){
    return{
      events:[
      {
        id:1,
        category:'Animal welfare',
        title:'Cat adoption day',
        description:'Find your feline friend at this event',
        location:'Pet Store',
        date:'January 28,2022',
        time:'12:00',
        petsAllowed:true,
        organizer:'Pet Lovers Inc'
      },
      {
        id:2,
        category:'Animal welfare',
        title:'Community Gardening',
        description:'Find your feline friend at this event',
        location:'Pet Store',
        date:'January 29,2022',
        time:'13:00',
        petsAllowed:true,
        organizer:'Pet Lovers Inc'
      },
      {
        id:3,
        category:'Animal welfare',
        title:'Beach Cleanup',
        description:'Find your feline friend at this event',
        location:'Pet Store',
        date:'January 30,2022',
        time:'14:00',
        petsAllowed:true,
        organizer:'Pet Lovers Inc'
      }
    ]
    }
  }
};
</script>

<style scoped>
.events{
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
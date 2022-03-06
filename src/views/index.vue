<template>
  <div>
    <attendee-board />
  </div>
</template>

<script>
import AttendeeBoard from "../components/AttendeeBoard.vue";
export default {
  name: "indexVue",

  components: { 
    AttendeeBoard, 
  },
};
</script>

<template>
  <v-card class="mx-auto mt-16" max-width="500">
    <v-card-text>
      <p class="text-h4 text--primary">Attendance of the Course</p>
      <div class="text--primary mt-8">
        <h2 v-if="selected !== '' && selected !== 0">
          {{ selected }}
        </h2>
      </div>
    </v-card-text>
    <v-card-actions>
      <v-btn class="primary" @click="select"> Select an Attendee</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: {
    attendees: {
      type: Array,
      required: true,
    },
    selected: {
      type: String,
      default: "",
      required: false,
    },
    allSelected: {
      type: Array,
      required: false,
    }
  },
  data() {
    return {};
  },
  methods: {
    select() {
      const val = Math.floor(Math.random() * this.attendees.length);
      if (val !== 0) {
        const selected = this.attendees[val].name;
        this.$emit("select", selected);
      }
    },
  },
};
</script>

<style scoped>
.card {
  margin: 0px auto;
  margin-top: 100px;
  width: 300px;
}
.selectedAttendees {
  float: left;
}
</style>

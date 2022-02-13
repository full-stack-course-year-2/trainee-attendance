<template>
  <div class="mt-16">
    <random :attendees="attendees" :selected="selected" @select="onSelect" />
  </div>
</template>

<script>
import Random from "./Random.vue";
export default {
  components: {
    Random,
  },
  data() {
    return {
      attendees: [
        { name: "01-Ahmet" },
        { name: "02-Mehmet" },
        { name: "03-Osman" },
        { name: "04-Okan" },
        { name: "06-Ahmet" },
        { name: "07-Mehmet" },
        { name: "08-Osman" },
        { name: "09-Okan" },
        { name: "10-Ahmet" },
        { name: "11-Mehmet" },
        { name: "12-Osman" },
        { name: "13-Okan" },
      ],
      selected: "",
    };
  },
  methods: {
    onSelect(payload) {
      this.selected = payload;
    },
  },
};
</script>

<style scoped>
.card {
  margin: 0px auto;
  width: 300px;
}
</style>

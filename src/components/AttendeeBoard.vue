<template>
  <div class="mt-16">
    <random :attendees="attendees" :selected="selected" @select="onSelect" />
    <div class="selectedPersons">
        <ul class="list-group">
            <li class="list-group-item" 
                :key="selectedPerson" 
                v-for="selectedPerson in allSelected">{{ selectedPerson }}
            </li>
        </ul>
    </div>
  </div>
</template>

<script>
import Random from "./RandomAttendees.vue";
export default {
  components: {
    Random,
  },
  data() {
    return {
      attendees: [
        { name: "1-Abdullah" },
        { name: "2-Ahmet" },
        { name: "3-Mahmut " },
        { name: "4-Cengiz" },
        { name: "5-Fatih" },
        { name: "6-Fatih" },
        { name: "7-Hatip" },
        { name: "8-Hilal" },
        { name: "9-Ibrahim" },
        { name: "10-Emre" },
        { name: "11-Mehmet" },
        { name: "12-Hakan" },
        { name: "13-Muhammet" },
        { name: "14-Mustafa" },
        { name: "15-Ercan" },
        { name: "16-Ramazan" },
        { name: "17-Ramis" },
        { name: "18-Resat" },
        { name: "19-Reyhan" },
        { name: "20-Senol" },
        { name: "21-Serdar" },
        { name: "22-Tarkan" },
        { name: "23-Tulin" },
        { name: "24-Yasar" },
        { name: "25-Yasin" },
        { name: "26-Yavuz" },       
      ],
      selected: [],
      answered: [],
      allSelected: []
    };
  },
  methods: {
    onSelect(payload) {
      this.selected = payload;
      this.allSelected.push(this.selected);
    },
  },
};
</script>

<style scoped>
.card {
  margin: 0px auto;
  width: 300px;
}
.selectedPersons {
  float: left;
  margin-left: 80px;
  width: 200px;
  font-size: 20px;
}
</style>

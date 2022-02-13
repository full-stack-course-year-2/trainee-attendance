<template>
  <v-card class="mx-auto mt-16" max-width="344">
    <v-card-text>
      <div>
        <v-chip class="ma-2"> Kursiyer Sec </v-chip>
      </div>
      <div class="text--primary mt-8">
        <h2 v-if="selected !== '' && selected !== 0">
          {{ selected }}
        </h2>
      </div>
    </v-card-text>
    <v-card-actions class="mt-8">
      <v-btn class="primary" @click="select"> Soru Sor </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      kursiyerArr: [
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
    select() {
      const val = Math.floor(Math.random() * this.kursiyerArr.length);
      if (val !== 0) this.selected = this.kursiyerArr[val].name;
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
</style>

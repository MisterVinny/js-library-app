<template>
  <div class="calendar">
    <h1>{{ title }}</h1>
    <div>
      <input type="text" id="datepicker" />
      <p>{{ pikaTime }}</p>
    </div>
    <div>
      <h1>{{ titleDatepicker }}</h1>
      <date-picker v-model="time1" valueType="format"></date-picker>
      <date-picker v-model="time2" type="datetime"></date-picker>
      <date-picker v-model="time3" range></date-picker>
      <p>Time 1: {{ time1 }}</p>
      <p>Time 2: {{ time2 }}</p>
      <p>Time 3: {{ time3 }}</p>
    </div>
  </div>
</template>

<script>
import Pikaday from "pikaday";
import "pikaday/css/pikaday.css";
import DatePicker from "vue2-datepicker";
import "vue2-datepicker/index.css";

export default {
  components: { DatePicker },
  data: function () {
    return {
      title: "I'm The Pikaday Calendar!",
      titleDatepicker: "I'm the Vue 2 Date Picker!",
      time1: null,
      time2: null,
      time3: null,
      pikaTime: null,
    };
  },

  mounted: function () {
    var picker = new Pikaday({
      field: document.getElementById("datepicker"),
      format: "YYYY-M-D",
    });
    console.log(picker);
  },
};
</script>

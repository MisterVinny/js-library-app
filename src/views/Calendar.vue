<template>
  <div class="calendar">
    <h1>{{ title }}</h1>
    <div>
      <input type="text" id="datepicker" />
    </div>
  </div>
</template>

<script>
import Pikaday from "pikaday";
import "pikaday/css/pikaday.css";

export default {
  data: function () {
    return {
      title: "I'm The Calendar!",
    };
  },

  mounted: function () {
    var picker = new Pikaday({ field: document.getElementById("datepicker") });
    console.log(picker);
  },
};
</script>

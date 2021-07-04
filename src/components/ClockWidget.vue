<template>
  <div class="clock-widget">
    <h4 class="clock-title">This is the current time</h4>
    <p class="clock-time">{{ currentDateTimeString }}</p>
  </div>
</template>

<script>
const momentTz = require("moment-timezone");
const SECOND_IN_MILLISECONDS = 1000;
export default {
  name: "ClockWidget",
  data() {
    return {
      currentDateTime: momentTz().tz("Asia/Manila"),
      dateTimeUpdater: null,
    };
  },
  beforeMount() {
    this.dateTimeUpdater = setInterval(
      this.updateDateTime,
      SECOND_IN_MILLISECONDS
    );
  },
  beforeUnmount() {
    clearInterval(this.dateTimeUpdater);
    this.dateTimeUpdater = null;
  },
  computed: {
    currentDateTimeString() {
      return this.currentDateTime.format();
    },
  },
  methods: {
    updateDateTime() {
      this.currentDateTime = momentTz().tz("Asia/Manila");
    },
  },
};
</script>

<style scoped>
.clock-widget * {
  margin: 0;
}
</style>

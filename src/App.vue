<script>
export default {
  data() {
    return {
      timeInput: '',
      timeDisplay: ''
    };
  },
  methods: {
    startTimer() {
      const timeInputValue = parseInt(this.timeInput);
      if (timeInputValue > 0 && timeInputValue <= 60) {
        this.timeDisplay = `Time remaining: ${timeInputValue} seconds`;
        let time = timeInputValue;

        const countdown = setInterval(() => {
          if (time > 0) {
            time--;
            this.timeDisplay = `Time remaining: ${time} seconds`;
          } else {
            clearInterval(countdown);
            alert("The timer has reached 0, start again?");
          }
        }, 1000);
      } else {
        alert("Please enter a valid time between 1-60 seconds)");
      }
    }
  }
};
</script>

<template>
  <div class="content">
    <div>
      <h1 class="main-title"> A Simple Count Down Timer</h1>
      <h2 class="center-text">by Kevin Dunn</h2>
  </div>
  <div class="formItems">
    <input v-model="timeInput" type="number" placeholder="Enter Seconds" />
    <button @click="startTimer" type="button">Start Timer</button>
  </div>
  <div id="timerDisplay" class="timerDisplay">{{ timeDisplay }}</div>
</div>

</template>


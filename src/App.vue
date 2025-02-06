<script setup>

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


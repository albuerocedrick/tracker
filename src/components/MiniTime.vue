<template>
    <div class="box flex flex-col justify-center items-center">
      <h1 class="font-bold text-5xl text-white">{{ currentTime }}</h1>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        currentTime: '',
        timer: null
      }
    },
    methods: {
      updateCurrentTime() {
        const now = new Date();
        
        // You can use toLocaleTimeString with options for more control
        this.currentTime = now.toLocaleTimeString(undefined, {
          hour: '2-digit',
          minute: '2-digit',
          second: '2-digit',
          hour12: true // set to false for 24-hour format
        });
      }
    },
    created() {
      // Set initial time
      this.updateCurrentTime();
      
      // Update time every second
      this.timer = setInterval(() => {
        this.updateCurrentTime();
      }, 1000);
    },
    beforeUnmount() {
      // Clean up the timer to prevent memory leaks
      if (this.timer) {
        clearInterval(this.timer);
      }
    }
  }
  </script>
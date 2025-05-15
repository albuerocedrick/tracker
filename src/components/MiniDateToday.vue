<template>
    <div class="box flex flex-col justify-center items-center">
      <p class="font-bold text-5xl text-white">{{ currentDate }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'CurrentDateComponent',
    data() {
      return {
        currentDate: this.getFormattedDate()
      };
    },
    methods: {
      getFormattedDate() {
        const today = new Date();
        const options = { year: 'numeric', month: 'long', day: 'numeric' };
        return today.toLocaleDateString(undefined, options);
      }
    }
  };
  </script>
  
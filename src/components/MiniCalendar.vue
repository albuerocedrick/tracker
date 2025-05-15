<template>
    <div :class="['mini-calendar p-4 border box w-full rounded-lg h-full flex flex-col', theme?.border]">
      <div class="header flex justify-between items-center mb-3 bg-[#7a6ca3] rounded-lg px-2">
        <button @click="prevMonth" class="text-lg p-1 text-white font-bold">&lt;</button>
        <span class="font-bold text-base text-white">{{ monthName }} {{ year }}</span>
        <button @click="nextMonth" class="text-lg p-1 text-white font-bold">&gt;</button>
      </div>
      <div class="days grid grid-cols-7 text-center">
        <div :class="['day text-md font-bold py-2', theme?.textColor]" v-for="day in daysOfWeek" :key="day">{{ day }}</div>
      </div>
      <div class="dates grid grid-cols-7 text-center flex-auto">
        <div
          v-for="date in dates"
          :key="date.key"
          :class="[
                    'date py-2 text-md font-medium cursor-pointer flex justify-center text-center items-center',
                    {
                      'text-gray-500': !date.isCurrentMonth,
                      'bg-[#7a6ca3] text-white rounded-full': date.isToday
                    },
                    !date.isToday && date.isCurrentMonth ? theme?.textColor : ''
                  ]"
        >
          {{ date.day }}
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'MiniCalendar',
    props:['theme'],
    data() {
      return {
        currentDate: new Date(),
        daysOfWeek: ['Su', 'Mo', 'Tu', 'We', 'Th', 'Fr', 'Sa'],
      };
    },
    computed: {
      year() {
        return this.currentDate.getFullYear();
      },
      month() {
        return this.currentDate.getMonth();
      },
      monthName() {
        return this.currentDate.toLocaleString('default', { month: 'long' });
      },
      dates() {
        const firstDayOfMonth = new Date(this.year, this.month, 1);
        const lastDayOfMonth = new Date(this.year, this.month + 1, 0);
        const startDay = firstDayOfMonth.getDay();
        const daysInMonth = lastDayOfMonth.getDate();
        const today = new Date();
        const dates = [];
  
        // Previous month's trailing days
        const prevMonthLastDay = new Date(this.year, this.month, 0).getDate();
        for (let i = startDay - 1; i >= 0; i--) {
          dates.push({
            day: prevMonthLastDay - i,
            isCurrentMonth: false,
            isToday: false,
            key: `prev-${i}`,
          });
        }
  
        // Current month's days
        for (let i = 1; i <= daysInMonth; i++) {
          const isToday =
            i === today.getDate() &&
            this.month === today.getMonth() &&
            this.year === today.getFullYear();
          dates.push({
            day: i,
            isCurrentMonth: true,
            isToday,
            key: `curr-${i}`,
          });
        }
  
        // Next month's starting days
        const totalSlots = Math.ceil((startDay + daysInMonth) / 7) * 7;
        for (let i = 1; dates.length < totalSlots; i++) {
          dates.push({
            day: i,
            isCurrentMonth: false,
            isToday: false,
            key: `next-${i}`,
          });
        }
  
        return dates;
      },
    },
    methods: {
      prevMonth() {
        this.currentDate = new Date(this.year, this.month - 1, 1);
      },
      nextMonth() {
        this.currentDate = new Date(this.year, this.month + 1, 1);
      },
    },
  };
  </script>
<template>
    <div
          class="grid grid-cols-4 grid-rows-4 gap-4">
            <MiniCompletedTask 
              class="cols-span-1 row-span-1 bg-[#7a6ca3]" 
              :class="theme.border"/>
            <MiniPendingTaskVue
              class="cols-span-1 row-span-1 bg-[#9bb587]"
              :class="theme.border"   />
            <MiniCalendar 
                class="col-span-2 row-span-2"
                :class="theme.cardBg"
                :theme="theme"/>
            <MiniUpcomingDeadline
              class="col-span-2 row-span-3"
              :class="theme.cardBg" 
              :theme="theme"/>
            <div class="col-span-2 row-span-2 grid grid-cols-2 grid-rows-2 gap-4">
                <MiniProjectList
                  class="row-span-2 col-span-1"
                  :class="theme.cardBg" 
                  :theme="theme"/>
                <MiniDateToday class="row-span-1 col-span-1 bg-[#7a6ca3]" :class="theme.border"/>
                <MiniTime class="row-span-1 col-span-1 bg-[#cfbfaf]" :class="theme.border"/>
            </div>
        </div>
</template>

<script>
import MiniPendingTaskVue from './MiniPendingTask.vue';
import MiniCompletedTask from './MiniCompletedTask.vue';
import MiniProjectList from './MiniProjectList.vue';
import MiniCalendar from './MiniCalendar.vue';
import MiniUpcomingDeadline from './MiniUpcomingDeadline.vue';
import MiniDateToday from './MiniDateToday.vue';
import MiniTime from './MiniTime.vue';

export default {
    components: {
        MiniPendingTaskVue,
        MiniCompletedTask,
        MiniProjectList,
        MiniCalendar,
        MiniUpcomingDeadline,
        MiniDateToday,
        MiniTime
    },
    props: ['theme']
}
</script>
<template>
    <div
          class="grid grid-cols-4 grid-rows-4 gap-4">
            <MiniCompletedTask 
              class="cols-span-1 row-span-1 bg-green-400" 
              :class="theme.border"/>
            <MiniPendingTaskVue
              class="cols-span-1 row-span-1 bg-red-400"
              :class="theme.border"   />
            <MiniCalendar 
                class="col-span-2 row-span-2"
                :class="theme.cardBg"
                :theme="theme"
                />
            <MiniUpcomingDeadline
              class="col-span-2 row-span-3"
              :class="theme.cardBg" 
              :theme="theme"
              @clickMenu="forwardClickMenu"/>
            <div class="col-span-2 row-span-2 grid grid-cols-2 grid-rows-2 gap-4">
                <MiniProjectList
                  class="row-span-2 col-span-1"
                  :class="theme.cardBg" 
                  :theme="theme"
                  @clickMenu="forwardClickMenu"/>
                <MiniMissedTask 
                  class="row-span-2 col-span-1"
                  :class="theme.cardBg"
                  :theme="theme"/>
            </div>
        </div>
</template>

<script>
import MiniPendingTaskVue from './MiniPendingTask.vue';
import MiniCompletedTask from './MiniCompletedTask.vue';
import MiniProjectList from './MiniProjectList.vue';
import MiniCalendar from './MiniCalendar.vue';
import MiniUpcomingDeadline from './MiniUpcomingDeadline.vue';
import MiniMissedTask from './MiniMissedTask.vue';

export default {
    components: {
        MiniPendingTaskVue,
        MiniCompletedTask,
        MiniProjectList,
        MiniCalendar,
        MiniUpcomingDeadline,
        MiniMissedTask,
    },
    props: ['theme'],
    emits: ['clickMenu'],
    methods: {      
      forwardClickMenu(index) {
        this.$emit('clickMenu', index);
      }
    }
}
</script>
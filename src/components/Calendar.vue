<template>
    <div class="flex flex-row gap-4" >
        <div class="w-2/3" >
            <mini-calendar 
                :class="[theme.cardBg, theme.border]"
                :theme="theme"/>
        </div>
        <div class="box w-1/3" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-[#9bb587] rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl">Tasks for Selected Date</div>
        </div>
    </div>
</template>

<script>
import MiniCalendar from './MiniCalendar.vue';

export default {
    props: ['theme'],
    components: {
        MiniCalendar,
    },
    props: ['theme'],
}
</script>
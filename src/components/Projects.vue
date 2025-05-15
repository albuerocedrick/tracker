<template>
    <div class="flex flex-row gap-4">
        <div class="box w-2/5" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-yellow-200 rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl">All Projects</div>
        </div>
        <div class="box w-3/5" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-yellow-200 rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl">In Progress</div>
        </div>
    </div>
</template>

<script>
import MiniCalendar from './MiniCalendar.vue';

export default {
    components: {
        MiniCalendar,
    },
    props: ['theme'],
}
</script>
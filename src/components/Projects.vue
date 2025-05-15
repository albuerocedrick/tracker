<template>
    <div class="flex flex-row gap-4">
        <div class="box w-2/5" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-[#7a6ca3] text-white rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl">All Projects</div>
        </div>
        <div class="box w-3/5 " :class="[theme.cardBg, theme.border]">
            <div class="flex flex-row flex-wrap gap-4 p-4">
                <div class="h-36 rounded-2xl p-4 bg-[#7a6ca3]/75 w-[49%] ">
                    <p></p>
                </div>
                <div class="h-36  rounded-2xl p-4 bg-[#7a6ca3]/75 w-[49%] ">
                    <p></p>
                </div>
                <div class="h-36  rounded-2xl p-4 bg-[#7a6ca3]/75 w-[49%] ">
                    <p></p>
                </div>
                <div class="h-36  rounded-2xl p-4 bg-[#7a6ca3]/75 w-[49%] ">
                    <p></p>
                </div>
                <div class="h-36  rounded-2xl p-4 bg-[#7a6ca3]/75 w-[49%] ">
                    <p></p>
                </div>
            </div>
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
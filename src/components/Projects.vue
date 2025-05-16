<template>
    <div class="flex flex-row gap-4">
        <div class="box w-2/5" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-[#a2cffe]  rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl">All Projects</div>
            <div class="flex flex-row items-center gap-4  rounded-md h-16 px-2 mb-2  mx-4 mt-4 shadow-md hover:bg-[#a2cffe]/30">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 7v10a2 2 0 002 2h14a2 2 0 002-2V9a2 2 0 00-2-2h-6l-2-2H5a2 2 0 00-2 2z" />
                </svg>
                <p class="font-medium whitespace-nowrap overflow-hidden text-ellipsis"> Library Management Project</p>
            </div>
        </div>
        <div class="box w-3/5 " :class="[theme.cardBg, theme.border]">
            <div class="flex flex-row flex-wrap gap-4 p-4">
                <div class="h-36 rounded-2xl p-4 hover:bg-[#a2cffe]/30 w-[49%] shadow-md ">
                    <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Create a Dashboard</p>
                    <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                </div>
                <div class="h-36 rounded-2xl p-4 hover:bg-[#a2cffe]/30 w-[49%] shadow-md ">
                    <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Create a Dashboard</p>
                    <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                </div>
                <div class="h-36 rounded-2xl p-4 hover:bg-[#a2cffe]/30 w-[49%] shadow-md ">
                    <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Create a Dashboard</p>
                    <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                </div>
                <div class="h-36 rounded-2xl p-4 hover:bg-[#a2cffe]/30 w-[49%] shadow-md ">
                    <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Create a Dashboard</p>
                    <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                </div>
                <div class="h-36 rounded-2xl p-4 hover:bg-[#a2cffe]/30 w-[49%] shadow-md ">
                    <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Create a Dashboard</p>
                    <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                </div>
                <div class="h-36 rounded-2xl p-4 hover:bg-[#a2cffe]/30 w-[49%] shadow-md ">
                    <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Create a Dashboard</p>
                    <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
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
    data() {
        return {
            taskShow: false,
        }
    }
}
</script>
<template>
    <div :class="['box', theme?.border]">
        <div class="flex flex-row justify-between items-center h-16 bg-red-400 rounded-t-2xl mb-2 p-2">
            <p :class="['font-bold text-xl', theme?.textColor]">Missed Tasks</p>
            <a href="#" :class="['font-semibold text-md ', theme.bg === 'bg-[#F4F3F2]' ? 'text-black/60' : 'text-white/60']">View All</a>
        </div>
        <div class="flex flex-row items-center gap-4 rounded-md h-12 px-2 mb-2  mx-2 hover:bg-red-400/30 justify-between shadow-md">
            <p class="font-medium whitespace-nowrap overflow-hidden text-ellipsis">Magsaing</p><br>
            <p class="text-black/60">Due Date: 10/25/2024</p>
        </div>
    </div>
</template>

<script>
export default {
    props: ['theme', 'task']
}
</script>
<template>
    <div :class="['box', theme?.border]">
        <div class="flex flex-row justify-between items-center h-16 bg-green-400 rounded-t-2xl mb-2 p-2">
            <p :class="['font-bold text-xl', theme?.textColor]">Projects</p>
            <a href="#" :class="['font-semibold text-md ', theme.bg === 'bg-[#F4F3F2]' ? 'text-black/60' : 'text-white/60']" @click="$emit('clickMenu', 2)">View All</a>
        </div>
        <div class="flex flex-row items-center gap-4 rounded-md h-12 px-2 mb-2  mx-2 hover:bg-green-400/30 shadow-md">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 7v10a2 2 0 002 2h14a2 2 0 002-2V9a2 2 0 00-2-2h-6l-2-2H5a2 2 0 00-2 2z" />
            </svg>
            <p class="font-medium whitespace-nowrap overflow-hidden text-ellipsis">{{ projects.title }}</p>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['theme'],
        emits: ['clickMenu'],
        data() {
            return {
                projects: {
                    title: 'Library Management'
                }
            }
        }
    }
</script>
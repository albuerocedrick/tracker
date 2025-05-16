<template>
    <div :class="['box', theme?.border]">
        <div class="flex flex-row justify-between mb-4 bg-[#a2cffe] rounded-t-2xl h-20  items-center px-4"> 
            <p :class="['font-semibold text-2xl', theme?.textColor]">Upcoming Deadline</p>
            <a href="#" :class="['font-semibold text-xl ', theme.bg === 'bg-[#F4F3F2]' ? 'text-black/60' : 'text-white/60']" @click="$emit('clickMenu', 1)">View All</a>
        </div>
        <div class="flex flex-row items-center hover:bg-[#a2cffe]/30 rounded-2xl mx-2  shadow-md mb-5">
            <input type="checkbox" class="h-5 w-5 ml-2">
            <div class=" h-20 rounded-xl flex-1 py-2 px-4 overflow-x-hidden overflow-y-visible flex flex-row justify-between items-center">
                <div>
                    <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis ">{{ task.Title }}</p>
                    <p class="text-black/60">Due Date: {{ task.Deadline }}</p>
                </div>
            </div>
        </div>
        <div class="flex flex-row items-center hover:bg-[#a2cffe]/30 rounded-2xl mx-2 shadow-md mb-5">
            <input type="checkbox" class="h-5 w-5 ml-2">
            <div class=" h-20 rounded-xl flex-1 py-2 px-4 overflow-x-hidden overflow-y-visible flex flex-row justify-between items-center">
                <div>
                    <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis ">{{ task.Title }}</p>
                    <p class="text-black/60">Due Date: {{ task.Deadline }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['theme'],
        emits: ['clickMenu'],
        data() {
            return {
                task: {
                    taskId: 1,
                    Title: 'Create a Dashboard',
                    Deadline: 'Oct. 17, 2025',
                    status: 'not started'
                },
                isOpen: false,
            }
        },
        methods: {
            ToggleDropdown() {
                this.isOpen = !this.isOpen;
            }
        }
    }
</script>
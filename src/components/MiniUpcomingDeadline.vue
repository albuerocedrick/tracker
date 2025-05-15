<template>
    <div :class="['box p-4', theme?.border]">
        <div class="flex flex-row justify-between mb-4"> 
            <p :class="['font-semibold text-2xl', theme?.textColor]">Upcoming Deadline</p>
            <a href="#" :class="['font-semibold text-xl ', theme.bg === 'bg-[#F4F3F2]' ? 'text-black/60' : 'text-white/60']" @click="$emit('clickMenu', 1)">View All</a>
        </div>
        <div class="flex flex-row w-full items-center">
            <div
              class=" w-7 h-7 mr-3 rounded-full"
              :class="[{'bg-yellow-500': task.status === 'pending'},
                        {'bg-green-500': task.status === 'completed'},
                        {'bg-red-500': task.status === 'not started'},
              ]"></div>
            <div class="bg-[#7a6ca3]/75 h-20 rounded-xl flex-1 py-2 px-4 overflow-x-hidden overflow-y-visible flex flex-row justify-between items-center">
                <div>
                    <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis text-white">{{ task.Title }}</p>
                    <p class="text-white/60">Due Date: {{ task.Deadline }}</p>
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
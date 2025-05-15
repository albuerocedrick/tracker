<template>
    <div class="box flex flex-col justify-center items-center text-center">
        <p class="font-bold text-5xl text-white">{{ completedTask }}</p>
        <p class="text-white font-medium text-xl" v-if="completedTask === 1">Task Completed</p>
        <p class="text-white font-medium text-xl" v-else-if="completedTask > 1">Tasks Completed</p>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                completedTask: 20,
            }
        }
    }
</script>
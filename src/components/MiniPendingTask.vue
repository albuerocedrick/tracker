<template>
    <div class="box flex flex-col justify-center items-center text-center">
        <p class="font-bold text-5xl text-white">{{ pendingTask }}</p>
        <p class="text-white font-medium text-xl" v-if="pendingTask === 1">Pending Task</p>
        <p class="text-white font-medium text-xl" v-else-if="pendingTask > 1">Pending Tasks </p>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                pendingTask: 1,
            }
        }
    }
</script>
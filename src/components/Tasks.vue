<template>
    <div class="flex flex-row gap-4">
        <div class="box w-1/3" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-red-400 rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl">Not Started</div>
            <div class="h-36  rounded-2xl m-4 p-4" :class="theme.bg">
                <p></p>
            </div>
        </div>
        <div class="box w-1/3" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-yellow-200 rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl">In Progress</div>
        </div>
        <div class="box w-1/3" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-green-400 rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl">Completed</div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['theme'],
}
</script>
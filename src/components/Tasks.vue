<template>
    <div class="flex flex-row gap-4">
        <div class="box w-1/3" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-[#7a6ca3] rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl text-white">Not Started</div>
            <div class="h-36  rounded-2xl m-4 p-4 bg-[#7a6ca3]/75">
                <p></p>
            </div>
            <div class="h-36  rounded-2xl m-4 p-4 bg-[#7a6ca3]/75">
                <p></p>
            </div>
            <div class="h-36  rounded-2xl m-4 p-4 bg-[#7a6ca3]/75">
                <p></p>
            </div>
        </div>
        <div class="box w-1/3" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-[#cfbfaf] rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl text-white">In Progress</div>
            <div class="h-36  rounded-2xl m-4 p-4 bg-[#7a6ca3]/75">
                <p></p>
            </div>
        </div>
        <div class="box w-1/3" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-[#9bb587] rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl text-white">Completed</div>
            <div class="h-36  rounded-2xl m-4 p-4 bg-[#7a6ca3]/75">
                <p></p>
            </div><div class="h-36  rounded-2xl m-4 p-4 bg-[#7a6ca3]/75">
                <p></p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['theme'],
}
</script>
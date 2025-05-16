<template>
    <div class="flex flex-row gap-4">
        <div class="box w-1/3" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-[#7a6ca3] rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl text-white">Not Started</div>
            <div class="h-36  rounded-2xl m-4 p-4 bg-[#7a6ca3]/75 hover-effect overflow-y-hidden">
                <div>
                    <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis text-white">Magluto ng Hotdog</p>
                    <p class="text-white/60 mb-2">Due Date: 10/17/2025</p>
                    <div class="flex flex-row">
                        <!-- <div class="h-12 w-40 rounded-3xl flex items-center overflow-hidden bg-[#cfbfaf] text-white py-2">
                            <svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8 flex-shrink-0 px-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 7v10a2 2 0 002 2h14a2 2 0 002-2V9a2 2 0 00-2-2h-6l-2-2H5a2 2 0 00-2 2z" />
                            </svg>
                             <p class="font-medium ">Library Management</p>
                        </div> -->
                    </div>
                </div>
            </div>
            <div class="h-36  rounded-2xl m-4 p-4 bg-[#7a6ca3]/75 hover-effect">
                <p></p>
            </div>
            <div class="h-36  rounded-2xl m-4 p-4 bg-[#7a6ca3]/75 hover-effect">
                <p></p>
            </div>
        </div>
        <div class="box w-1/3" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-[#cfbfaf] rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl text-white">In Progress</div>
            <div class="h-36  rounded-2xl m-4 p-4 bg-[#7a6ca3]/75 hover-effect">
                <p></p>
            </div>
        </div>
        <div class="box w-1/3" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-[#9bb587] rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl text-white">Completed</div>
            <div class="h-36  rounded-2xl m-4 p-4 bg-[#7a6ca3]/75 hover-effect">
                <p></p>
            </div><div class="h-36  rounded-2xl m-4 p-4 bg-[#7a6ca3]/75 hover-effect">
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
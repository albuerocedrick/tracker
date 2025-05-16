<template>
    <div class="flex flex-row gap-4">
        <div class="box w-1/4" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-gray-400 rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl ">Not Started</div>
            <div class="h-24  rounded-2xl m-4 overflow-y-hidden p-2 shadow-md hover:bg-gray-400/30">
                <div class="flex flex-col justify-center align-center">
                    <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Magluto ng Hotdog</p>
                    <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                </div>
            </div>
            <div class="h-24  rounded-2xl m-4 overflow-y-hidden p-2 shadow-md hover:bg-gray-400/30">
                <div class="flex flex-col justify-center align-center">
                    <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Magluto ng Hotdog</p>
                    <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                </div>
            </div>
            <div class="h-24  rounded-2xl m-4 overflow-y-hidden p-2 shadow-md hover:bg-gray-400/30">
                <div class="flex flex-col justify-center align-center">
                    <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Magluto ng Hotdog</p>
                    <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                </div>
            </div>
        </div>
        <div class="box w-1/4" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-blue-400 rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl black">In Progress</div>
            <div class="h-36  rounded-2xl">
                <div class="h-24  rounded-2xl m-4 overflow-y-hidden p-2 shadow-md hover:bg-gray-400/30">
                    <div class="flex flex-col justify-center align-center">
                        <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Magluto ng Hotdog</p>
                        <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                    </div>
                </div>
                <div class="h-24  rounded-2xl m-4 overflow-y-hidden p-2 shadow-md hover:bg-gray-400/30">
                    <div class="flex flex-col justify-center align-center">
                        <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Magluto ng Hotdog</p>
                        <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="box w-1/4" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-green-400 rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl ">Completed</div>
            <div class="h-36  rounded-2xl">
                <div class="h-24  rounded-2xl m-4 overflow-y-hidden p-2 shadow-md hover:bg-gray-400/30">
                    <div class="flex flex-col justify-center align-center">
                        <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Magluto ng Hotdog</p>
                        <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="box w-1/4" :class="[theme.cardBg, theme.border]">
            <div class="h-24 bg-red-400 rounded-t-2xl flex justify-center text-center items-center font-bold text-3xl">Missed</div>
            <div class="h-36  rounded-2xl">
                <div class="h-24  rounded-2xl m-4 overflow-y-hidden p-2 shadow-md hover:bg-gray-400/30">
                    <div class="flex flex-col justify-center align-center">
                        <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Magluto ng Hotdog</p>
                        <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                    </div>
                </div>
                <div class="h-24  rounded-2xl m-4 overflow-y-hidden p-2 shadow-md hover:bg-gray-400/30">
                    <div class="flex flex-col justify-center align-center">
                        <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Magluto ng Hotdog</p>
                        <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                    </div>
                </div>
                <div class="h-24  rounded-2xl m-4 overflow-y-hidden p-2 shadow-md hover:bg-gray-400/30">
                    <div class="flex flex-col justify-center align-center">
                        <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Magluto ng Hotdog</p>
                        <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                    </div>
                </div>
                <div class="h-24  rounded-2xl m-4 overflow-y-hidden p-2 shadow-md hover:bg-gray-400/30">
                    <div class="flex flex-col justify-center align-center">
                        <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Magluto ng Hotdog</p>
                        <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                    </div>
                </div>
                <div class="h-24  rounded-2xl m-4 overflow-y-hidden p-2 shadow-md hover:bg-gray-400/30">
                    <div class="flex flex-col justify-center align-center">
                        <p class="font-medium text-2xl whitespace-nowrap overflow-hidden text-ellipsis">Magluto ng Hotdog</p>
                        <p class="text-black/60 mb-2">Due Date: 10/17/2025</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['theme'],
}
</script>
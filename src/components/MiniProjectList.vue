<template>
    <div :class="['box p-4', theme?.border]">
        <h1 :class="['font-bold text-xl pb-4', theme?.textColor]">Projects</h1>
        <div class="flex flex-row items-center gap-4 bg-[#cfbfaf] rounded-md h-12 px-2 mb-2 text-white">
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
        data() {
            return {
                projects: {
                    title: 'Library Management'
                }
            }
        }
    }
</script>
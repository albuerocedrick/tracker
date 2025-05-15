<template>
    <div class="box" :class="[theme.cardBg, theme.border]">
        <div :class="[ 'h-20 m-4 rounded-2xl flex flex-row justify-between items-center', 
                        theme.bg === 'bg-[#F4F3F2]' ? 'hover:bg-[#f4f3f2]' :' hover:bg-gray-900'
        ] ">
            <p :class="['font-medium pl-4', theme.textColor]">Dark Mode</p>
            <!-- Large Toggle with Custom Colors - Tailwind Only Solution -->
            <div class="relative inline-block w-20 align-middle select-none">
            <!-- Hidden checkbox for state -->
            <input type="checkbox" id="toggle" class="sr-only peer" :checked="theme.bg === 'bg-gray-900'" @click="ChangeTheme">
            
            <!-- Toggle background -->
            <div class="w-20 h-8 rounded-full bg-[#f4f3f2] peer-checked:bg-gray-900 transition-colors duration-300"></div>
            
            <!-- Toggle circle -->
            <div class="absolute left-0 top-0 bg-[#7a6ca3] w-8 h-8 rounded-full transition-transform duration-300 peer-checked:translate-x-12"></div>
            
            <!-- Clickable label covering the entire toggle -->
            <label for="toggle" class="absolute inset-0 cursor-pointer"  ></label>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['theme', 'ChangeTheme']
    }
</script>
<template>
    <div :class="[theme.cardBg, 'h-20', 'box', theme.border, 'flex', 'flex-row', 'items-center', 'justify-between']">
        <div>
            <h1 :class="['font-bold', 'text-2xl', 'm-8', theme.textColor]">Assignment and Activity Tracker</h1>
        </div>
        <div class=" h-full rounded-2xl flex flex-row items-center justify-between px-4 gap-4">
            
            
            <!-- Notification Bell -->
            <div class=" rounded-full h-14 w-14 flex items-center justify-center overflow-hidden mt-2" :class="theme.textColor">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="-30 -40 60 80" class="w-12 h-12">
                <!-- Bell -->
                <path d="M-18,-15 C-18,-25 -10,-35 0,-35 C10,-35 18,-25 18,-15 L18,5 L22,15 L-22,15 L-18,5 Z" fill="none" stroke="currentColor" stroke-width="8" stroke-linejoin="round"/>
                <!-- Bell clapper -->
                <circle cx="0" cy="0" r="3" fill="currentColor"/>
                <!-- Notification dot -->
                <!-- <circle cx="12" cy="-25" r="6" fill="currentColor"/> -->
                <!-- Bell bottom -->
                <path d="M-5,15 C-5,22 5,22 5,15" fill="none" stroke="currentColor" stroke-width="8" stroke-linecap="round"/>
                </svg>
            </div>
            <!-- Profile Icon -->
            <div :class="[' rounded-full h-14 w-14 flex items-center justify-center overflow-hidden', theme.textColor]">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="-45 -45 90 90" class="w-12 h-12">
                <!-- Circle background -->
                <circle cx="0" cy="0" r="40" fill="none" stroke="currentColor" stroke-width="8"/>
                <!-- Head -->
                <circle cx="0" cy="-12" r="16" fill="currentColor"/>
                <!-- Body -->
                <path d="M-24,15 C-24,0 24,0 24,15 L24,24 C24,30 -24,30 -24,24 Z" fill="currentColor"/>
                </svg>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  props: ['theme']
}
</script>
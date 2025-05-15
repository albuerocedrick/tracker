<template>
    <div :class=" [theme.cardBg, 'h-20', 'box', theme.border, 'flex', 'flex-row', 'items-center', 'justify-between']">
        <h1 :class="['font-bold', 'text-2xl', 'm-8', theme.textColor]">  Assignment and Activity Tracker</h1>
    </div>
</template>

<script>
    export default {
        props: ['theme']
    }
</script>
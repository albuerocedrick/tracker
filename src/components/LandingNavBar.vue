<template>
    <div :class=" [theme.cardBg, 'h-20', 'box', theme.border, 'flex', 'flex-row', 'items-center', 'justify-between']">
        <h1 :class="['font-bold', 'text-2xl', 'm-8', theme.textColor]">  Assignment and Activity Tracker</h1>
        <ul class="flex flex-row justify-evenly w-1/5">
            <li
              v-for="(page, index) in landingPages"
              :key="index">
                <a
                  @click.prevent="$emit('NavModalOpen', index)"
                  :href="page.link.url"
                  :class="['font-medium', theme.textColor, index === landingPages.length - 1 ? 'log-in-btn' : '']">{{ page.link.label }}</a>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        props: ['landingPages', 'theme'],
        emits: ['NavModalOpen']
    }
</script>

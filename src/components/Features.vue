<template>
    <div class="flex flex-row gap-4 mt-4">
        <div
          :class="['box', theme.border, 'h-75', theme.cardBg, 'w-1/3', 'flex', 'flex-col', 'justify-center', 'gap-4', 'items-center']"
          v-for="(feature, index) in features"
          :key="index">
            <img
              class="w-20"
              :src="feature.imgpath"
              :alt="feature.alt">
            <h1 :class="['font-extrabold', 'text-4xl', theme.textColor]">{{ feature.title }}</h1>
            <p :class="['font-semibold', theme.textColor]">{{ feature.desc }}</p>
        </div>
    </div>
</template>

<script>
    import UsersIcon from '../assets/UsersIcon.png';
    import DashBoardIcon from '../assets/DashBoardIcon.png';
    import ClockIcon from '../assets/ClockIcon.png';

    export default {
        props: ['theme'],
        data() {
            return {
                features: [
                    {  
                        title: 'Real-Time Collaboration', 
                        desc: 'Work with others and assign tasks instantly. Updates sync in real-time.',
                        alt: 'users icon',
                        imgpath: UsersIcon
                                
                    },
                    {
                        title: 'Deadline Reminders', 
                        desc: 'Get notified before your tasks are due.',
                        alt: 'clock icon',
                        imgpath: ClockIcon
                    },
                    {
                        title: 'Progress Dashboard', 
                        desc: 'See your task progress in one place.',
                        alt: 'dashboard icon',
                        imgpath:  DashBoardIcon
                    },
                ]
            }
        },
    }
</script>

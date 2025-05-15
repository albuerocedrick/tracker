<template>
    <div class="flex flex-row">
        <div class="flex-1 flex flex-col justify-center items-center text-center gap-8 px-28">
            <h1 :class="['text-4xl', 'md:text-5xl', 'font-bold', theme.textColor]">Streamline Your Tasks and Collaborate Effortlessly with Assignment and Activity Tracker</h1>
            <p :class="['text-md', 'md:text-xl', theme.textColor]">A powerful task management tool that allows you to seamlessly collaborate with others. By giving selective access, other users can assign tasks to you, helping you stay on top of your assignments and activities in real-time.</p>
            <button class="w-2xs h-16 rounded-xl text-white bg-[#7a6ca3] font-medium shadow hover-effect" @click.prevent="$emit('NavModalOpen', 2)"> Get Started</button>       
        </div>
        <div class="flex-1 flex justify-center items-center ">
            <img src="../assets/clipboard.png" alt="clipboard image">
        </div>
    </div>
</template>

<script>
export default {
    props: ['theme'],
    emits: ['NavModalOpen']
}
</script>
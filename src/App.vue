<template >
    <div
      v-if="landingPageShow"
      :class="[theme.bg, 'p-4']">
        <LandingNavBar 
            :landing-pages="landingPages"
            :theme="theme"
            @NavModalOpen="NavModalOpen"
        />
        <HeroSection
            :class="['h-screen', 'box', theme.border , theme.cardBg, 'flex', 'justify-center', 'items-center', 'mt-4']"
            :theme="theme" 
            @NavModalOpen="NavModalOpen"/>
        <Features
            :theme="theme" />
        <LogInPage
            v-show="logInShow" 
            :theme="theme"
            @NavModalClose="NavModalClose"
            @OpenMainPage="OpenMainPage"/>
        <SignUpPage
            v-show="SignUpShow"
            :theme="theme"
            @NavModalClose="NavModalClose"
            @OpenMainPage="OpenMainPage"/>    
    </div>

    <div
    v-else
      class="p-4 w-screen h-screen grid grid-rows-[80px_1fr] grid-cols-[300px_1fr] gap-4"
      :class="[theme.bg]">
        <MainNavBar
            class="col-span-2"
            :theme="theme"
            :selectedMenu="selectedMenu"/>
        <SideBar class="h-full" :class="[theme.border, theme.cardBg] " @ClickMenu="clickMenu" :selectedMenu="selectedMenu" :theme="theme"/>
        <dashb 
            v-show="selectedMenu === 0"
            :theme="theme"
            @clickMenu="clickMenu"/>
        <tasks 
            v-show="selectedMenu === 1"
            :theme="theme"/>
        <projects 
            v-show="selectedMenu === 2"
            :theme="theme"/>
        <calendar 
            v-show="selectedMenu === 3"
            :theme="theme"/>
        <settings 
            v-show="selectedMenu === 4"
            :theme="theme"
            :ChangeTheme="ChangeTheme"/>
        
    </div>
</template>

<script>
import LandingNavBar from './components/LandingNavBar.vue'
import HeroSection from './components/HeroSection.vue';
import Features from './components/Features.vue';
import LogInPage from './components/LogInPage.vue';
import SignUpPage from './components/SignUpPage.vue';
import MainNavBar from './components/MainNavBar.vue';
import SideBar from './components/SideBar.vue';
import Dashb from './components/Dashb.vue';
import Tasks from './components/Tasks.vue';
import Projects from './components/Projects.vue';
import Calendar from './components/Calendar.vue';
import Settings from './components/Settings.vue';

export default {
    components: {
        LandingNavBar,
        HeroSection,
        Features,
        LogInPage,
        SignUpPage,
        MainNavBar,
        SideBar,
        Dashb,
        Tasks,
        Projects,
        Calendar,
        Settings
    },
    created() {
        this.theme = this.GetLocalTheme();
    },
    data() {
        return {
            selectedMenu: 0,
            theme: {
                bg: 'bg-[#F4F3F2]',
                cardBg: 'bg-[#EBE8E2]',
                textColor: 'text-black',
                border: 'border-black'
            },
            landingPages: [
                {
                link: {label: 'About Us', url: 'aboutus.html' }
                },
                {
                link: {label: 'Log In', url: 'login.html' }
                },
                {
                link: {label: 'Sign Up', url: 'signup.html' }
                },
            ],
            aboutUsShow: false,
            logInShow: false,
            SignUpShow: false,
            landingPageShow: true,
            
        }
    },
    methods: {
        ChangeTheme() {
            if (this.theme.cardBg === 'bg-white') {
                this.theme.bg = 'bg-gray-900';
                this.theme.cardBg = 'bg-gray-950';
                this.theme.textColor = 'text-white';
                this.theme.border = 'border-gray-600'
            } else {
                this.theme.bg = 'bg-[#F4F3F2]';
                this.theme.cardBg = 'bg-[#EBE8E2]';
                this.theme.textColor = 'text-black';
                this.theme.border = 'border-black';
            }

            this.SetLocalTheme();
        },
        SetLocalTheme() {
            localStorage.setItem('theme', JSON.stringify(this.theme));
        },
        GetLocalTheme() {
            let theme = JSON.parse(localStorage.getItem('theme'));
            return theme ? theme : this.theme;
        },
        NavModalOpen(index) {
            if(index === 0) {
                this.aboutUsShow = true;
                this.logInShow = this.SignUpShow = false;
            }
            else if(index === 1) {
                this.logInShow = true;
                this.aboutUsShow = this.SignUpShow = false;
            } 
            else if(index === 2) {
                this.SignUpShow = true;
                this.aboutUsShow = this.logInShow = false;
            }
        },
        NavModalClose() {
            if(this.aboutUsShow || this.logInShow || this.SignUpShow) {
                this.aboutUsShow = this.logInShow = this.SignUpShow = false;
            }
        },
        OpenMainPage() {
            this.landingPageShow = false;
        },
        clickMenu(index) {
            this.selectedMenu = index;
        }
    }
}

</script>

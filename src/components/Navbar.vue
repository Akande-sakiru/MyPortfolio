<!-- <template>
    <nav class="fixed top-0 w-full z-50 bg-slate-950/90 backdrop-blur">
        <div class="max-w-7xl mx-auto px-6 h-20 flex justify-between items-center">
            <h1 class="text-cyan-400 font-bold text-2xl">
                Sakiru.
            </h1>

            <ul class="hidden md:flex gap-8">
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>
</template> -->

<template>
    <nav :class="[
        'fixed top-0 left-0 w-full z-50 transition-all duration-300',
        scrolled
            ? 'bg-slate-950/90 backdrop-blur-md shadow-lg'
            : 'bg-transparent'
    ]">
        <div class="container">
            <div class="nav-wrapper">

                <!-- Logo -->
                <a href="#" class="logo">
                    Sakiru<span>.</span>
                </a>

                <!-- Desktop Menu -->
                <ul class="desktop-menu">
                    <li v-for="item in menuItems" :key="item.id">
                        <a :href="item.link">
                            {{ item.name }}
                        </a>
                    </li>
                </ul>

                <!-- Hire Me -->
                <a href="#contact" class="hire-btn">
                    Hire Me
                </a>

                <!-- Mobile Menu Button -->
                <button class="mobile-btn" @click="mobileMenu = !mobileMenu">
                    <Menu v-if="!mobileMenu" :size="28" />
                    <X v-else :size="28" />
                </button>

            </div>
        </div>

        <!-- Mobile Menu -->
        <transition name="slide">
            <div v-if="mobileMenu" class="mobile-menu">
                <a v-for="item in menuItems" :key="item.id" :href="item.link" @click="mobileMenu = false">
                    {{ item.name }}
                </a>

                <a href="#contact" class="mobile-hire" @click="mobileMenu = false">
                    Hire Me
                </a>
            </div>
        </transition>
    </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";
import { Menu, X } from "lucide-vue-next";

const mobileMenu = ref(false);
const scrolled = ref(false);

const menuItems = [
    {
        id: 1,
        name: "About",
        link: "#about"
    },
    {
        id: 2,
        name: "Skills",
        link: "#skills"
    },
    {
        id: 3,
        name: "Experience",
        link: "#experience"
    },
    {
        id: 4,
        name: "Projects",
        link: "#projects"
    },
    {
        id: 5,
        name: "Contact",
        link: "#contact"
    }
];

const handleScroll = () => {
    scrolled.value = window.scrollY > 50;
};

onMounted(() => {
    window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
    window.removeEventListener("scroll", handleScroll);
});
</script>

<style scoped>
.container {
    max-width: 1300px;
    margin: auto;
    padding: 0 24px;
}

.nav-wrapper {
    height: 80px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    color: white;
    text-decoration: none;
    font-size: 28px;
    font-weight: 800;
}

.logo span {
    color: #06b6d4;
}

.desktop-menu {
    display: flex;
    gap: 35px;
    list-style: none;
}

.desktop-menu a {
    color: white;
    text-decoration: none;
    transition: .3s;
}

.desktop-menu a:hover {
    color: #06b6d4;
}

.hire-btn {
    background: #06b6d4;
    color: white;
    padding: 12px 24px;
    border-radius: 12px;
    text-decoration: none;
    font-weight: 600;
}

.mobile-btn {
    display: none;
    background: none;
    border: none;
    color: white;
}

.mobile-menu {
    background: #020617;
    display: flex;
    flex-direction: column;
    padding: 20px;
}

.mobile-menu a {
    color: white;
    text-decoration: none;
    padding: 15px 0;
}

.mobile-hire {
    background: #06b6d4;
    padding: 12px;
    border-radius: 10px;
    text-align: center;
    margin-top: 10px;
}

.slide-enter-active,
.slide-leave-active {
    transition: .3s;
}

.slide-enter-from,
.slide-leave-to {
    opacity: 0;
    transform: translateY(-10px);
}

@media(max-width:768px) {

    .desktop-menu,
    .hire-btn {
        display: none;
    }

    .mobile-btn {
        display: block;
    }
}
</style>
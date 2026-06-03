<template>
    <section class="min-h-screen flex items-center justify-center bg-slate-950 text-white">
        <div class="text-center">

            <p class="text-cyan-400 uppercase tracking-widest">
                Full Stack Software Engineer
            </p>

            <h1 class="text-6xl font-black mt-4">
                Sakiru Akande
            </h1>

            <h2 class="text-3xl mt-4 text-slate-300">
                <span ref="typedElement"></span>
            </h2>

            <p class="max-w-2xl mt-8 mx-auto text-slate-400">
                Building scalable ERP systems,
                student information systems,
                SaaS applications and enterprise software
                using Laravel and Vue.js.
            </p>

            <div class="mt-8 flex justify-center gap-4">
                <a href="#projects" class="px-8 py-4 bg-cyan-500 rounded-lg">
                    View Projects
                </a>

                <a href="#contact" class="px-8 py-4 border rounded-lg">
                    Hire Me
                </a>
            </div>
        </div>
    </section>
</template>

<script setup>
import Typed from "typed.js";
import { onMounted, ref } from "vue";

const typedElement = ref(null);

onMounted(() => {
    new Typed(typedElement.value, {
        strings: [
            "Laravel Developer",
            "Vue.js Engineer",
            "API Architect",
            "EdTech Solution Builder",
        ],
        typeSpeed: 60,
        backSpeed: 40,
        loop: true,
    });
});
</script>
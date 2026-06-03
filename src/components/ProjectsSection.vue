<template>
    <section id="projects" class="py-32 bg-slate-900">
        <div class="max-w-7xl mx-auto">

            <h2 class="text-center text-4xl font-bold mb-20">
                Featured Projects
            </h2>

            <div class="grid md:grid-cols-2 gap-10">
                <div v-for="project in projects" :key="project.title" class="bg-slate-800 rounded-xl overflow-hidden">
                    <img :src="project.image" class="w-full" />

                    <div class="p-6">

                        <h3 class="text-2xl font-bold">
                            {{ project.title }}
                        </h3>

                        <p class="mt-4">
                            {{ project.description }}
                        </p>

                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import projects from "../data/projects";
</script>
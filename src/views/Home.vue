<template>
    <Navbar />

    <section id="hero">
        <HeroSection />
    </section>

    <section id="about">
        <AboutSection />
    </section>

    <section id="skills">
        <SkillsSection />
    </section>

    <section id="experience">
        <ExperienceSection />
    </section>

    <section id="projects">
        <ProjectsSection />
    </section>

    <section id="services">
        <ServicesSection />
    </section>

    <section id="stats">
        <StatsSection />
    </section>

    <section id="testimonials">
        <TestimonialsSection />
    </section>

    <section id="contact">
        <ContactSection />
    </section>

    <Footer />
</template>

<script setup>
import Navbar from "../components/Navbar.vue";
import HeroSection from "../components/HeroSection.vue";
import AboutSection from "../components/AboutSection.vue";
import SkillsSection from "../components/SkillsSection.vue";
import ExperienceSection from "../components/ExperienceSection.vue";
import ProjectsSection from "../components/ProjectsSection.vue";
import ServicesSection from "../components/ServicesSection.vue";
import StatsSection from "../components/StatsSection.vue";
import TestimonialsSection from "../components/TestimonialsSection.vue";
import ContactSection from "../components/ContactSection.vue";
import Footer from "../components/Footer.vue";
</script>
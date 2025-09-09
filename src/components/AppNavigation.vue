<template>
    <nav class="fixed top-0 left-0 right-0 z-50 bg-white/90 backdrop-blur-lg border-b border-gray-200">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- Logo -->
                <div class="flex items-center space-x-2">
                    <div class="w-8 h-8 bg-gradient-to-br from-teal-200 to-teal-400 rounded-lg flex items-center justify-center">
                        <MessageSquare class="w-5 h-5 text-teal-700 font-bold" />
                    </div>
                    <span class="text-xl font-bold text-teal-700">Cyrene</span>
                </div>

                <!-- Desktop Navigation -->
                <div class="hidden md:flex items-center space-x-8">
                    <a href="#how-it-works" class="text-gray-600 hover:text-teal-700 font-medium transition-colors"> How It Works </a>
                    <a href="#use-cases" class="text-gray-600 hover:text-teal-700 font-medium transition-colors"> Use Cases </a>
                    <a href="#features" class="text-gray-600 hover:text-teal-700 font-medium transition-colors"> Features </a>
                    <a href="#pricing" class="text-gray-600 hover:text-teal-700 font-medium transition-colors"> Pricing </a>
                </div>

                <!-- CTA Button -->
                <div class="flex items-center space-x-4">
                    <button class="bg-teal-200 text-teal-700 font-bold px-6 py-2 rounded-md hover:bg-teal-300 hover:text-teal-800 transition-all duration-200 shadow-sm hover:shadow-md">Start Free Trial</button>

                    <!-- Mobile Menu Button -->
                    <button @click="toggleMobileMenu" class="md:hidden p-2 rounded-md text-gray-600 hover:text-teal-700 hover:bg-teal-50 transition-colors">
                        <Menu v-if="!mobileMenuOpen" class="w-6 h-6" />
                        <X v-else class="w-6 h-6" />
                    </button>
                </div>
            </div>

            <!-- Mobile Menu -->
            <div v-if="mobileMenuOpen" class="md:hidden py-4 border-t border-gray-200 bg-white/95 backdrop-blur-lg">
                <div class="flex flex-col space-y-4">
                    <a href="#how-it-works" @click="mobileMenuOpen = false" class="text-gray-600 hover:text-teal-700 font-medium py-2"> How It Works </a>
                    <a href="#use-cases" @click="mobileMenuOpen = false" class="text-gray-600 hover:text-teal-700 font-medium py-2"> Use Cases </a>
                    <a href="#features" @click="mobileMenuOpen = false" class="text-gray-600 hover:text-teal-700 font-medium py-2"> Features </a>
                    <a href="#pricing" @click="mobileMenuOpen = false" class="text-gray-600 hover:text-teal-700 font-medium py-2"> Pricing </a>
                </div>
            </div>
        </div>
    </nav>
</template>

<script setup>
import { ref } from "vue";
import { MessageSquare, Menu, X } from "lucide-vue-next";

const mobileMenuOpen = ref(false);

const toggleMobileMenu = () => {
    mobileMenuOpen.value = !mobileMenuOpen.value;
};
</script>

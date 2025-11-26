<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pasindu Abeysundara - Web Developer Portfolio</title>
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Load Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <!-- Configure Tailwind -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        // Using a deeper, more consistent dark gray based on the sample image
                        'main-bg': '#191919', // Deep dark gray for background
                        'card-bg': '#242424', // Slightly lighter dark gray for cards
                        'accent-blue': '#3b82f6', // Bright blue accent
                        'accent-light': '#a0a0a0', // Light gray for subtle text
                        'text-primary': '#ffffff', // White text
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap');
        
        /* Custom scroll down button animation */
        .scroll-down-icon {
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-10px);
            }
            60% {
                transform: translateY(-5px);
            }
        }

        /* Ensure the main container matches the viewport height for better centering */
        .hero-container {
            min-height: calc(100vh - 80px); /* Subtract header height */
        }
    </style>
</head>
<body class="bg-main-bg text-text-primary font-sans min-h-screen">

    <!-- Navbar -->
    <header class="sticky top-0 z-20 bg-main-bg/95 backdrop-blur-sm shadow-xl">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <!-- Logo -->
            <a href="#" class="flex items-center text-2xl font-bold text-accent-blue tracking-wider">
                <i data-lucide="code" class="w-6 h-6 mr-2"></i> Developer X
            </a>
            <!-- Navigation Links -->
            <nav class="hidden md:flex space-x-6 text-sm font-medium text-gray-300">
                <a href="#home" class="hover:text-accent-blue transition duration-200">Home</a>
                <a href="#about" class="hover:text-accent-blue transition duration-200">About</a>
                <a href="#blog" class="hover:text-accent-blue transition duration-200">Blog</a>
                <a href="#portfolio" class="hover:text-accent-blue transition duration-200">Portfolio</a>
                <div class="group relative">
                    <button class="flex items-center hover:text-accent-blue transition duration-200">
                        Pages <i data-lucide="chevron-down" class="w-4 h-4 ml-1"></i>
                    </button>
                    <!-- Simple Dropdown Placeholder -->
                    <div class="absolute right-0 mt-2 w-48 bg-card-bg rounded-lg shadow-xl hidden group-hover:block border border-gray-700">
                        <a href="#" class="block px-4 py-2 text-sm hover:bg-gray-700 rounded-lg">Page 1</a>
                        <a href="#" class="block px-4 py-2 text-sm hover:bg-gray-700 rounded-lg">Page 2</a>
                    </div>
                </div>
            </nav>
            <!-- Mobile Menu Icon -->
            <button class="md:hidden text-gray-300 hover:text-accent-blue transition duration-200" onclick="toggleMobileMenu()">
                <i data-lucide="menu" class="w-6 h-6"></i>
            </button>
        </div>
        <!-- Mobile Menu (Hidden by default) -->
        <div id="mobile-menu" class="hidden md:hidden bg-card-bg">
            <a href="#home" class="block px-4 py-2 text-base hover:bg-gray-700">Home</a>
            <a href="#about" class="block px-4 py-2 text-base hover:bg-gray-700">About</a>
            <a href="#blog" class="block px-4 py-2 text-base hover:bg-gray-700">Blog</a>
            <a href="#portfolio" class="block px-4 py-2 text-base hover:bg-gray-700">Portfolio</a>
            <a href="#" class="block px-4 py-2 text-base hover:bg-gray-700">Pages</a>
        </div>
    </header>

    <!-- Hero Section (Replicating the main image layout) -->
    <main id="home" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-16 hero-container">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-start h-full">
            
            <!-- Left/Center Main Content (8/12 grid columns) -->
            <div class="lg:col-span-8 relative flex flex-col lg:flex-row items-end h-full">
                <!-- Large Profile Photo -->
                <div class="relative w-full lg:w-3/4 order-2 lg:order-1">
                    <!-- 
                         Updated to use your Google Drive Link.
                         Note: If this link fails to load due to Google Drive permissions, 
                         it will fall back to the placeholder.
                    -->
                    <img 
                        src="https://drive.google.com/uc?export=view&id=1CWgr7_3K5iUy55Q9o8RYefseaKibJsCV" 
                        alt="Pasindu Abeysundara Profile" 
                        class="w-full h-auto object-cover rounded-xl shadow-2xl opacity-90"
                        onerror="this.onerror=null; this.src='https://placehold.co/600x700/191919/d1d5db?text=Image+Load+Error';"
                    >
                </div>

                <div class="w-full order-1 lg:order-2 lg:absolute lg:bottom-0 lg:left-0 lg:w-4/5 lg:-mb-16 bg-main-bg lg:bg-transparent p-0 pb-16 lg:p-0">
                    <div class="w-20 h-1 bg-white mb-4"></div>
                    <h1 class="text-4xl sm:text-6xl lg:text-7xl font-extrabold leading-tight">
                        I'm Pasindu, a <br>
                        <span class="text-accent-blue">Web Developer</span>
                    </h1>
                    <p class="mt-4 text-lg text-accent-light max-w-xl">
                        A passionate Full Stack Engineer specializing in modern JavaScript frameworks (React, Node.js) and clean, scalable architecture.
                    </p>
                    
                    <!-- Scroll Down Button -->
                    <a href="#about" class="mt-8 inline-flex items-center justify-center w-16 h-16 rounded-full bg-accent-blue hover:bg-blue-600 transition duration-300 shadow-xl cursor-pointer">
                        <i data-lucide="chevron-down" class="w-8 h-8 text-white scroll-down-icon"></i>
                    </a>
                </div>
            </div>

            <!-- Right Sidebar Content (4/12 grid columns) -->
            <div class="lg:col-span-4 space-y-8 pt-10" id="about">
                
                <!-- About Me Block -->
                <div class="p-6 bg-card-bg rounded-xl shadow-xl border border-gray-800">
                    <h2 class="text-sm font-semibold uppercase text-accent-light mb-3 tracking-widest">ABOUT ME</h2>
                    <p class="text-text-primary text-base">
                        With five years of experience, my focus is on building user-centric interfaces and optimizing backend services for speed and reliability.
                    </p>
                    <a href="#" class="mt-4 inline-flex items-center text-accent-blue font-medium hover:text-blue-400 transition duration-200">
                        LEARN MORE <i data-lucide="arrow-right" class="w-4 h-4 ml-2"></i>
                    </a>
                </div>

                <!-- My Work Block -->
                <div class="p-6 bg-card-bg rounded-xl shadow-xl border border-gray-800">
                    <h2 class="text-sm font-semibold uppercase text-accent-light mb-3 tracking-widest">MY WORK</h2>
                    <p class="text-text-primary text-base">
                        Explore recent case studies, including an e-commerce platform built with Next.js and a real-time data visualization dashboard.
                    </p>
                    <a href="#" class="mt-4 inline-flex items-center text-accent-blue font-medium hover:text-blue-400 transition duration-200">
                        BROWSE PORTFOLIO <i data-lucide="arrow-right" class="w-4 h-4 ml-2"></i>
                    </a>
                </div>

                <!-- Follow Me Block -->
                <div class="p-6 bg-card-bg rounded-xl shadow-xl border border-gray-800">
                    <h2 class="text-sm font-semibold uppercase text-accent-light mb-4 tracking-widest">FOLLOW ME</h2>
                    <div class="flex space-x-4">
                        <a href="https://facebook.com" target="_blank" class="text-accent-light hover:text-accent-blue transition duration-200" aria-label="Facebook">
                            <i data-lucide="facebook" class="w-6 h-6"></i>
                        </a>
                        <a href="https://twitter.com" target="_blank" class="text-accent-light hover:text-accent-blue transition duration-200" aria-label="Twitter">
                            <i data-lucide="twitter" class="w-6 h-6"></i>
                        </a>
                        <a href="https://instagram.com" target="_blank" class="text-accent-light hover:text-accent-blue transition duration-200" aria-label="Instagram">
                            <i data-lucide="instagram" class="w-6 h-6"></i>
                        </a>
                        <a href="https://linkedin.com" target="_blank" class="text-accent-light hover:text-accent-blue transition duration-200" aria-label="LinkedIn">
                            <i data-lucide="linkedin" class="w-6 h-6"></i>
                        </a>
                        <a href="https://github.com" target="_blank" class="text-accent-light hover:text-accent-blue transition duration-200" aria-label="GitHub">
                            <i data-lucide="github" class="w-6 h-6"></i>
                        </a>
                    </div>
                </div>
            </div>
            
        </div>
    </main>

    <!-- Footer (Simple Placeholder) -->
    <footer class="bg-card-bg border-t border-gray-800 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8 text-center text-sm text-gray-500">
            &copy; 2025 Pasindu Abeysundara. All rights reserved. | Built with HTML & Tailwind CSS.
        </div>
    </footer>

    <!-- Script to initialize Lucide icons -->
    <script>
        lucide.createIcons();

        // Simple mobile menu toggle
        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        }
    </script>
</body>
</html>

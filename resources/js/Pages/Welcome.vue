<script setup>
import NavLink from '@/Components/NavLink.vue';
import { Head, Link } from '@inertiajs/vue3';

defineProps({
    canLogin: {
        type: Boolean,
    },
    canRegister: {
        type: Boolean,
    },
    laravelVersion: {
        type: String,
        required: true,
    },
    phpVersion: {
        type: String,
        required: true,
    },
});
</script>

<template>
    <div class="max-h-screen h-screen">
        <div class="flex h-full">
            <div class="hidden lg:flex flex-col justify-between h-full w-[20%] border-r border-gray-300 pt-14">
                <nav class="bordder">
                    <ul class="flex flex-col gap-3 ml-10 text-[1.3rem]">
                        <li>
                            <NavLink :href="route('dashboard')" :active="route().current('dashboard')">Home</NavLink>
                        </li>
                        <li>
                            <NavLink :href="route('dashboard')" :active="route().current('dashboard')">Fashion</NavLink>
                        </li>
                        <li>
                            <NavLink :href="route('dashboard')" :active="route().current('dashboard')">Travel</NavLink>
                        </li>
                        <li>
                            <NavLink :href="route('dashboard')" :active="route().current('dashboard')">About</NavLink>
                        </li>
                        <li>
                            <NavLink :href="route('dashboard')" :active="route().current('dashboard')">Contact</NavLink>
                        </li>
                    </ul>
                </nav>
                <div class="flex flex-col pl-2 min-w-[12rem] gap-4">
                    <div class="image-container w-[100%]">
                        <h1
                            class="logo text-black bg-white font-bold md:text-[2.5rem] xl:text-[3.2rem] 2xl:text-[4rem] transition w-[100%] font-serif ">
                            <span class="drop-shadow-2xl">BLOG</span> <span>Building</span>
                        </h1>
                    </div>
                    <div class="flex flex-col items-center gap-y-4">
                        <div class="w-full">
                            <h2 class="mb-4 text-start font-bold">Abonnez-vous à la newsletter</h2>
                            <label for="newspaper" class="relative">
                                <input type="text" name="newspaper" id="newspaper" placeholder="Entrez Votre Email"
                                    class="border-1 border-blue-500 w-[80%]">
                                <span class="absolute rotate-[-45deg] right-3 top-[-30%] text-gray-500 hidden xl:block">
                                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"
                                        class="h-6 w-6">
                                        <path d="M2,21L23,12L2,3V10L17,12L2,14V21Z" />
                                    </svg>
                                </span>
                            </label>
                            <p class="text-start my-4 pr-4">Copyright ©2024 Tous droits réservés</p>
                        </div>
                    </div>
                </div>
            </div>


            <div class="lg:w-[80%] w-[100%] max-h-[100%] overflow-y-scroll flex">
                <div class="w-[70%] pt-20">
                    <!-- Container -->
                </div>
                <!-- Categories bar -->
                <!-- 2xl:bg-white -->
                <div class="w-[30%] hidden xl:block bg-gray-100">
                    <!-- 2xl:bg-gray-50 -->
                    <div class="2xl:w-[80%] pt-20 2xl:px-4 w-[90%] mx-auto h-full">
                        <!-- Search Input -->
                        <label for="newspaper" class="relative">
                            <input type="text" name="newspaper" id="newspaper" placeholder="Entrer le mot-clé"
                                class="border-1 border-blue-500 w-[100%]">
                            <span class="absolute right-3 top-[-20%] text-gray-500 hidden xl:block">
                                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"
                                    class="h-6 w-6">
                                    <path
                                        d="M9.5,3A6.5,6.5 0 0,1 16,9.5C16,11.11 15.41,12.59 14.44,13.73L14.71,14H15.5L20.5,19L19,20.5L14,15.5V14.71L13.73,14.44C12.59,15.41 11.11,16 9.5,16A6.5,6.5 0 0,1 3,9.5A6.5,6.5 0 0,1 9.5,3M9.5,5C7,5 5,7 5,9.5C5,12 7,14 9.5,14C12,14 14,12 14,9.5C14,7 12,5 9.5,5Z" />
                                </svg>
                            </span>
                        </label>
                        <!-- Search Input -->

                        <!-- Categories -->
                        <div class="mt-14">
                            <h2 class="mb-4 italic text-[1.4rem] font-serif">Catégories</h2>
                            <ul>
                                <li>
                                    <a href="#" class="categories_links"><span>Fashion</span><span>(5)</span></a>
                                </li>
                                <li>
                                    <a href="#" class="categories_links"><span>Technology</span><span>(41)</span></a>
                                </li>
                                <li>
                                    <a href="#" class="categories_links"><span>Travel</span><span>(8)</span></a>
                                </li>
                                <li>
                                    <a href="#" class="categories_links"><span>Food</span><span>(50)</span></a>
                                </li>
                                <li>
                                    <a href="#" class="categories_links"><span>Photography</span><span>(75)</span></a>
                                </li>

                            </ul>
                        </div>
                        
                        <!-- Categories -->

                        <div class="mt-14">
                            <h2 class="mb-4 italic text-[1.4rem] font-serif">Articles populaires</h2>
                            <ul>
                                <li>
                                    <div>
                                        <a href="#">
                                            <p>

                                            </p>
                                        </a>
                                    </div>
                                </li>
                                <li></li>
                                <li></li>
                                <li></li>
                            </ul>
                        </div>
                    </div>


                </div>
            </div>
        </div>
    </div>
</template>
<style>
/* 
* Logo background-image
 */
.image-container {
    background-image: url("@/../../public/images/title2.jpg");
    background-size: cover;
}

/**
* Logo text properties
 */
.logo {
    mix-blend-mode: screen;
}

/**
* Categories_links
*/
.categories_links {
    display: flex;
    justify-content: space-between;
    font-weight: bold;
    border-bottom: 1px solid rgb(151, 149, 149);
    margin-bottom: 1rem;
    padding: 0.5rem;
    color: rgb(167, 164, 164);
}
</style>


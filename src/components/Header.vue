<script>
    export default{
        data(){
            return{
                menu:false
            }
        },
    }
</script>

<template>
    <header class="">
        <div class="px-[10px] py-[20px] lg:py-[40px] flex justify-between items-center overflow-x-hidden lg:max-w-[1120px] lg:mx-auto">
            <a><img class="w-[80%]" src="/src/assets/logo.svg" alt=""></a>
            <button class="z-[1] lg:hidden" @click="mudarBody(menu = !menu) "><img :src="[menu ? '/src/assets/icon-menu-close.svg': '/src/assets/icon-menu.svg']" class="w-[100%]" alt=""></button>
            <nav class="absolute lg:static top-[0px] right-0 lg:h-auto lg:w-auto  duration-500 transition" :class="[menu ? 'bg-[rgba(0,0,0,0.6)] w-[100%] h-[100%]' : 'w-[0px] h-[0px]']">
                <ul class="absolute lg:static top-[0px] right-0 space-y-5 lg:space-y-0 lg:flex lg:space-x-5 lg:w-auto lg:h-auto lg:opacity-[1] lg:my-0 p-5 lg:p-0 lg:pt-[0rem] pt-[8rem] w-[60%] h-[100vh] lg:pointer-events-auto  bg-white lg:bg-transparent duration-500 transition" :class="[menu ? 'opacity-[1]' : 'opacity-0 pointer-events-none']">
                    <li><a href="#home" class="hover:text-Soft-red hover:transition hover:duration-300">Home</a></li>
                    <li><a href="#new" class="hover:text-Soft-red hover:transition hover:duration-300">New</a></li>
                    <li><a href="#popular" class="hover:text-Soft-red hover:transition hover:duration-300">Popular</a></li>
                    <li><a href="#trending" class="hover:text-Soft-red hover:transition hover:duration-300">Trending</a></li>
                    <li><a href="#categories" class="hover:text-Soft-red hover:transition hover:duration-300">Categories</a></li>
                </ul>
            </nav>
        </div>
    </header>
</template>
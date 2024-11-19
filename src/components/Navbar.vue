<template>
    <!-- Information Above Nav -->
    <div
        class="info-above-nav fixed top-0 z-10 w-full h-14 bg-[#23856D] flex-row justify-center gap-x-10 items-center text-white sm:hidden md:flex">
        <div class="w-fit h-fit flex flex-row">
            <img src="@/assets/img/icon/icon_phone.svg" alt="" class="w-4 h-4 my-auto mr-2" />
            <p class="text-xs font-normal">(225) 555-0118</p>
        </div>
        <div class="w-fit h-fit flex flex-row">
            <img src="@/assets/img/icon/icon_mail.svg" alt="" class="w-4 h-4 my-auto mr-1" />
            <p class="text-xs font-normal">michelle.rivera@example.com</p>
        </div>
        <div class="w-fit h-fit flex flex-row">
            <p class="text-sm font-bold">Follow Us and get a chance to win 80% off</p>
        </div>
        <div class="w-fit h-fit flex flex-row items-center">
            <p class="text-sm font-bold mr-2">Follow Us</p>
            <p class="text-sm font-bold mr-4">:</p>
            <div class="w-fit h-fit flex flex-row justify-between align-middle items-center gap-x-3">
                <img src="@/assets/img/icon/icon_instagram.svg" alt="" />
                <img src="@/assets/img/icon/icon_yt.svg" alt="" />
                <img src="@/assets/img/icon/icon_fb.svg" alt="" />
                <img src="@/assets/img/icon/icon_twitter.svg" alt="" />
            </div>
        </div>
    </div>

    <!-- Navigation -->
    <nav
        class="fixed sm:top-0 md:top-14 z-10 w-full sm:h-fit md:h-14 bg-white flex sm:flex-col md:flex-row justify-center gap-x-28 items-center">
        <div
            class="flex flex-row sm:w-full md:w-fit sm:justify-around sm:gap-x-28 md:gap-x-0 sm:mt-5 md:mt-0 sm:mb-5 md:mb-0">
            <h1 class="text-black text-2xl font-bold cursor-pointer">Bandage</h1>
            <img src="@/assets/img/icon/burger.svg" alt="" class="md:hidden" @click="toggleNav" />
        </div>
        <div
            :class="['w-fit h-fit', navVisible ? 'sm:flex' : 'sm:hidden', 'md:flex', 'sm:flex-col md:flex-row sm:text-center justify-between gap-x-5 sm:gap-y-4 md:gap-y-0 sm:mb-4 md:mb-0 sm:mt-6 md:mt-0 sm:font-normal md:font-bold sm:text-2xl md:text-sm text-[#737373]']">
            <a href="">
                <p class="sm:text-[#252B42] md:text-[#737373]">Home</p>
            </a>
            <a href="" class="flex flex-row w-auto h-fit">
                <p class="md:text-[#252B42] sm:mx-auto">Shop</p>
                <img src="@/assets/img/icon/arrow_down_shop.svg" alt="arrow_down"
                    class="sm:ml-0 md:ml-2 sm:hidden md:flex" />
            </a>
            <a href="">
                <p>About</p>
            </a>
            <a href="">
                <p>Blog</p>
            </a>
            <a href="">
                <p>Contact</p>
            </a>
            <a href="">
                <p>Pages</p>
            </a>
        </div>

        <div
            :class="['w-auto h-fit', navVisible ? 'sm:flex' : 'sm:hidden', 'md:flex', 'sm:flex-col md:flex-row justify-center items-center gap-x-7 sm:gap-y-5 md:gap-y-0 sm:mt-4 md:mb-0 sm:mb-4 md:mt-0']">
            <div class="w-fit h-fit flex flex-row items-center cursor-pointer">
                <img src="@/assets/img/icon/icon_user.svg" alt="" class="mr-2 sm:w-5 sm:h-5 md:w-fit md:h-fit" />
                <p class="sm:text-xl md:text-sm font-bold text-[#23A6F0]">Login / Register</p>
            </div>
            <div>
                <img src="@/assets/img/icon/icon_search.svg" alt=""
                    class="sm:w-7 sm:h-7 md:w-fit md:h-fit cursor-pointer" />
            </div>
            <div class="w-fit h-fit flex flex-row items-center cursor-pointer">
                <img src="@/assets/img/icon/icon_cart.svg" alt="" class="mr-1 sm:w-7 sm:h-7 md:w-fit md:h-fit" />
                <p class="text-xs font-normal text-[#23A6F0]">1</p>
            </div>
            <div class="w-fit h-fit flex flex-row items-center cursor-pointer sm:mb-4 md:mb-0">
                <img src="@/assets/img/icon/icon_nav_heart.svg" alt="" class="mr-1 sm:w-7 sm:h-7 md:w-fit md:h-fit" />
                <p class="text-xs font-normal text-[#23A6F0]">1</p>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            navVisible: false, D
        };
    },
    methods: {
        toggleNav() {
            this.navVisible = !this.navVisible;
        },
    },
};
</script>
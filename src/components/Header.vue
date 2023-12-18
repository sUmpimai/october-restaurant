<script setup>
import { ref } from 'vue'

const activeIndex = ref(0);
const isShowMobileNav = ref(false)

const setActive = (index) => {
  return activeIndex.value = index
}

const navMenuList = ref([
    {
        id: 0,
        name: 'home',
        link: '/home'
    },
    {
        id: 1,
        name: 'about',
        link: '/about'
    },
    {
        id: 2,
        name: 'menus',
        link: '/menus'
    },
    {
        id: 3,
        name: 'gallery',
        link: '/gallery'
    },
    {
        id: 4,
        name: 'reservation',
        link: '/reservation'
    },
    {
        id: 5,
        name: 'news',
        link: '/news'
    }
])
</script>

<template>
    <header class="border-b border-[rgba(255,255,255,0.1)] h-[60px] bg-transparent fixed top-0 z-40 w-full">
        <div class="max-w-7xl mx-auto relative py-4">
            <nav class="flex items-center">
                <a href="/" class="text-white">
                October Restaurant
                </a>
                <ul
                class="flex nav-bar ml-auto space-y-5 md:space-y-0"
                >
                    <li
                        v-for="(nav, index) in navMenuList"
                        @click="setActive(nav.id)"
                    >
                        <a 
                        href=""
                        :class="{active: activeIndex === nav.id}"
                        >
                        {{ nav.name }}
                        </a>
                    </li>
                </ul>
                <div class="ml-auto md:hidden">
                    <button 
                    type="button"
                    @click="showNavMobile(!isShowMobileNav)"
                    class="text-white w-8 h-8 flex items-center justify-center hover:text-white">
                        <svg width="24" height="24" fill="none" aria-hidden="true"><path d="M12 6v.01M12 12v.01M12 18v.01M12 7a1 1 0 1 1 0-2 1 1 0 0 1 0 2Zm0 6a1 1 0 1 1 0-2 1 1 0 0 1 0 2Zm0 6a1 1 0 1 1 0-2 1 1 0 0 1 0 2Z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path></svg>
                    </button>
                </div>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
.nav-bar {
    li {
        a {
            @apply uppercase text-[#ddd] text-xs tracking-wide font-medium px-3;
            &:hover,
            &.active {
                color: #fff;
                @apply font-semibold

            }
        }
    }
}

.offcanvas-right {
    ul {
        @apply fixed md:static top-0 right-0 bg-white md:bg-transparent p-5 w-60 md:w-full pt-16 md:pt-0 h-full;
        a {
            @apply text-black text-base;

            &:hover,
            &.active {
                @apply text-black;
            }
        }
    }
}
</style>
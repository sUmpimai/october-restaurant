<script setup>
import Hero from '../components/Hero.vue'
import Footer from '../components/Footer.vue'
import Menu from '../components/Menu.vue'
</script>

<template>
  <main>
    <Hero />
    <!-- our story -->
    <div class="max-w-7xl mx-auto px-7 md:px-5">
      <div class="flex items-center py-20 space-x-6">
      <div class="w-1/2">
        <h4 class="text-sm font-['Playfair'] italic text-[#777] pb-2">Sweet and tiny like a chocolate</h4>
        <h2 class="text-4xl font-extrabold uppercase pb-6">Our Story</h2>
        <p>Tincidunt integer eu augue augue nunc elit dolor luctus placerat scelerisque euismod iaculis eu lacus nunc mi elit vehicula ut laoreet acaliquam sit amet justo nunc tempor metus vel. Lorem ipsum dolor sit amet consectetur adipiscing elitsed do eiusmod tempor incididunt utlabore et dolore magna aliqua. Utenim ad minim veniam quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
      </div>
      <div class="w-1/2">
        <div class="h-96 bg-[url('https://images.unsplash.com/photo-1663530761401-15eefb544889')] bg-center bg-no-repeat bg-cover"></div>
      </div>
    </div>
    </div>
    <Menu />
    <Footer />
  </main>
</template>

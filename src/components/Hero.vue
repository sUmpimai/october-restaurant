<template>
    <div class="w-full h-screen bg-[url('https://images.unsplash.com/photo-1517248135467-4c7edcad34c4')] bg-center bg-no-repeat bg-cover">
       <div class="relative max-w-2xl mx-auto h-screen space-y-5 text-white text-center flex flex-col items-center justify-center z-20">
        <h1>The October Restaurant</h1>
        <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. It has survived not only five centuries.</p>
        <a href="">Make Reservation</a>
       </div>
       <div class="bg-gradient-to-t from-black absolute z-10 h-full w-full left-0 top-0"></div>
    </div>
</template>

<style lang="scss" scoped>
h1 {
    font-family: 'Playfair', sans-serif;
    @apply text-4xl text-6xl font-extrabold pb-5;
}

p {
    color: #ddd;
}

a {
    display: block;
    @apply block bg-transparent border border-white rounded-sm tracking-wider text-white text-xs uppercase px-7 py-3;

    &:hover {
        @apply bg-white text-black transition duration-500 ease-in-out;
    }
}
</style>
<script>
    import { ref } from "vue";
    export default
    {
        setup()
        {
            const navLinks = ref({
                Home: {
                    name: "Home",
                    href: "/"
                },
                VidGames: {
                    name: "Games",
                    href: "/about"
                },
                Series: {
                    name: "Series",
                    href: "#"
                }

            });
            return { navLinks };
        }
    };
</script>
<template>
    <div>
        <nav class ="lg:block bg-gray-900 bg-opacity-70 z-10">
            <ul class = "flex space-x-5 lg:space-x-8 items-center p-4">
                <li class="font-bold text-3xl text-red-600">GameFlix</li>
                <li v-for="link in navLinks" :key="link.name">
                    <router-link
                    :to="link.href"
                    class="font-bold text-sm lg;text-base text-white hover:text-app-green-1 transition ease-in-out duration-300">
                    {{ link.name }} 
                    </router-link>
                </li>
            </ul>
        </nav>
    </div>
</template>
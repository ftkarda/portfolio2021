<template>

<div class="relative w-full bg-white text-gray-700 font-mono">

<!-- wrapper -->
<div class="relative p-5 lg:px-32 flex flex-col md:flex-row items-center justify-center">

    <!-- Social Media -->
    <div class="w-full md:w-1/2 p-5 md:px-0 mx-5 ">
    <div class="bg-white border border-indigo-500 w-full lg:w-1/2 h-full p-5 pt-8 animate-fade-in-down">
        <h3 class="text-2xl font-semibold mb-5 leading-tight inline-flex border-b-2 border-indigo-500 pb-2">
        Follow Me
        </h3>
        <!-- list -->
        <div class="flex flex-col gap-3 ">
			
		<a href="https://github.com/ftkarda" class="flex items-center hover:text-white hover:bg-indigo-500 p-2">
         <i data-feather="github" class="w-6 h-6 m-2"></i>
            Ardha Fatika
        </a>
        <a href="https://www.linkedin.com/in/ftkarda/" class="flex items-center hover:text-white hover:bg-indigo-500 p-2">
            <i data-feather="linkedin" class="w-6 h-6 m-2"></i>
            Ardha Fatika
          
        </a>
        <a href="https://www.instagram.com/ftkarda/" class="flex items-center hover:text-white hover:bg-indigo-500 p-2">
            <i data-feather="instagram" class="w-6 h-6 m-2"></i>
            Ardha Fatika
        </a>
        <a href="https://www.facebook.com/ftkarda" class="flex items-center hover:text-white hover:bg-indigo-500 p-2">
            <i data-feather="facebook" class="w-6 h-6 m-2"></i>
            Ardha Fatika
        </a>
        </div>
    </div>
    </div>

    <!-- Contact Me -->
    <div class="w-full md:w-1/2 border border-indigo-500 p-6 animate-fade-in-down">
    <h2 class="text-2xl font-semibold leading-tight inline-flex border-b-2 border-indigo-500 pb-2 mb-5">
        Get In Touch
    </h2>
    <div>
        <div class="flex mb-3">
        <i data-feather="map-pin" class="w-5 text-gray-500 dark:text-gray-400 mr-4"></i>
			<p class="text-lg mb-4 text-ternary-dark dark:text-ternary-light">Jl Antapani, Bandung, Jawa Barat</p>
        </div>
        <div class="flex mb-3">
        <i data-feather="home" class="w-5 text-gray-500 dark:text-gray-400 mr-4"></i>
			<p class="text-lg mb-4 text-ternary-dark dark:text-ternary-light">Balikpapan, 05 Feb 1996</p>
        </div>
        <div class="flex mb-3">
       <i data-feather="phone" class="w-5 text-gray-500 dark:text-gray-400 mr-4"></i>
			<p class="text-lg mb-4 text-ternary-dark dark:text-ternary-light">085346741110</p>
        </div>
		<div class="flex mb-3">
			<i data-feather="mail" class="w-5 text-gray-500 dark:text-gray-400 mr-4"></i>
			<p class="text-lg mb-4 text-ternary-dark dark:text-ternary-light">fatikaardha@gmail.com</p>
        </div>
    </div>

    </div>
</div>
</div>

</template>

<script>
import feather from 'feather-icons';

export default {
	data: () => {
		return {};
	},
	mounted() {
		feather.replace();
	},
	updated() {
		feather.replace();
	},
	methods: {},
};
</script>

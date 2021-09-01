<template>
	<!-- Projects start -->
	<section class="pt-10 md:pt-20 sm:pt-10 font-mono">
		<div class="text-center animate-fade-in-down">
			<p class="text-2xl sm:text-5xl font-semibold text-indigo-500 leading-relaxed"
			>
				Portfolio
			</p>
			<p class="text-md sm:text-xl text-gray-500 border-b-2 border-indigo-500 inline-flex pb-2 leading-tight">
				My Project
			</p>
		</div>

		<div class="grid grid-cols-1 sm:grid-cols-3 mt-16 sm:gap-10 animate-fade-in-down">
			
			<router-link
				to="/projects"
				class="rounded-3xl shadow-lg hover:shadow-xl hover:opacity-75 cursor-default mb-10 sm:mb-0 bg-secondary-light dark:bg-ternary-dark"
			>
				<div class="relative shadow-lg hover:shadow-xl transition duration-500 rounded-lg">
					
					<img
						src="../../assets/images/portofolio/cvklik/cvklik5.jpg"
						alt=""
						class="rounded-t-3xl border-none"/>
					<div class="absolute top-2 right-2 py-1 px-2 bg-gray-100 rounded-lg">
						<span class="text-xs font-bold border-r-4 border-indigo-500 pr-1">Finished</span>
					</div>
				</div>
				<div class="text-center px-4 py-6">
					<p
						class="text-2xl text-ternary-dark dark:text-ternary-light font-semibold mb-2"
					>
						Company Profile
					</p>
					<span
						class="text-lg text-ternary-dark dark:text-ternary-light"
						>Responsive Website</span
					>
				</div>
			</router-link>
			<router-link
				to="/projects"
				class="rounded-3xl shadow-lg hover:shadow-xl hover:opacity-75 cursor-default mb-10 sm:mb-0 bg-secondary-light dark:bg-ternary-dark"
			>
				<div class="relative shadow-lg hover:shadow-xl transition duration-500 rounded-lg">
					<img
						src="../../assets/images/portofolio/halopajajaran/halopajajaran.jpg"
						alt=""
						class="rounded-t-3xl border-none"/>
						<div class="absolute top-2 right-2 py-1 px-2 bg-gray-100 rounded-lg">
						<span class="text-xs font-bold border-r-4 border-indigo-500 pr-1">Finished</span>
					</div>
				</div>
				<div class="text-center px-4 py-6">
					<p
						class="text-2xl text-ternary-dark dark:text-ternary-light font-semibold mb-2"
					>
						Maintance Website
					</p>
					<span
						class="text-lg text-ternary-dark dark:text-ternary-light"
						>Maintain Front-end Website</span
					>
				</div>
			</router-link>
			<router-link
				to="/projects/single-project"
				class="rounded-3xl shadow-lg hover:shadow-xl cursor-pointer mb-10 sm:mb-0 bg-secondary-light dark:bg-ternary-dark inset-0 transform  hover:scale-90 transition duration-700"
			>
				<div class="relative shadow-lg hover:shadow-xl transition duration-500 rounded-lg">
					<img
						src="../../assets/images/portofolio/klikshop/klikshop1.jpg"
						alt=""
						class="rounded-t-3xl border-none "/>
						<div class="absolute top-2 right-2 py-1 px-2 bg-indigo-500 rounded-lg">
						<span class="text-xs font-bold border-r-2 border-white text-white pr-1">New</span>
					</div>
				</div>
				<div class="text-center px-4 py-6">
					<p
						class="text-2xl text-ternary-dark dark:text-ternary-light font-semibold mb-2"
					>
						Project Online Shop
					</p>
					<span
						class="text-lg text-ternary-dark dark:text-ternary-light"
						>UI / Frontend</span
					>
				</div>
			</router-link>
		
		</div>
		<!-- <div class="mt-10 sm:mt-20 flex justify-center">
			<button
				class="flex items-center px-6 py-3 rounded-xl shadow-lg hover:shadow-xl bg-indigo-500 hover:bg-indigo-600 text-white text-lg sm:text-xl font-medium"
			>
				<i data-feather="refresh-cw" class="w-5 mr-3"></i>
				<span>Load More</span>
			</button>
		</div> -->
	</section>
	<!-- Projects end -->
</template>

<script>
import feather from 'feather-icons';

export default {
	name: 'Projects',
	mounted() {
		feather.replace();
	},
	updated() {
		feather.replace();
	},
};
</script>

<style scoped></style>

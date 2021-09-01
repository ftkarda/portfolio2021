<template>
	<div class="bg-gray-50 shadow-sm mt-20 animate-fade-in-down">
		
		<h2 class="font-mono text-2xl md:text-5xl font-bold pt-10 text-indigo-500 md:px-36 px-5 md:text-left text-center">Skills</h2>
        <p class=" border-b-2 border-indigo-500 text-gray-500 pb-2 text-sm md:text-xl md:mx-36 mx-5 md:text-left text-center inline-flex leading-tight">Here's some programming languages that i'm used</p>


		<div class="container block sm:flex sm:justify-between sm:items-center md:mt-5 mt-10 pb-10">
		
		<transition
			appear
			@before-enter="beforeEnter"
			@enter="enter"
			@after-enter="afterEnter">

		<div class="grid grid-cols-2 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 md:grid-cols-3 gap-2 mx-0 md:mx-3 sm:gap-10 md:gap-10 xl:gap-24 text-center font-mono">
			
			<div>
				<img
					src="../../assets/images/brands/html.png"
					alt=""
					class="w-64 py-5 px-10 border border-ternary-light dark:border-ternary-dark shadow-lg rounded-xl mb-8 cursor-default inset-0 transform hover:rotate-12 hover:scale-75 transition duration-300 hover:shadow-2xl"
				/> HTML
			</div>
			
			<div>
				<img
					src="../../assets/images/brands/css.png"
					alt=""
					class="w-64 py-5 px-10 border border-ternary-light dark:border-ternary-dark shadow-lg rounded-xl mb-8 cursor-default inset-0 transform hover:-rotate-12 hover:scale-75 transition duration-300 hover:shadow-2xl"
				/>CSS
			</div>
			<div>
				<img
					src="../../assets/images/brands/tailwind.png"
					alt=""
					class="w-64 py-5 px-10 border border-ternary-light dark:border-ternary-dark shadow-lg rounded-xl mb-8 cursor-default inset-0 transform hover:rotate-45 hover:scale-75 transition duration-300 hover:shadow-2xl"
				/>Framework Tailwind CSS
			</div>
			<div>
				<img
					src="../../assets/images/brands/bootstrap.png"
					alt=""
					class="w-64 py-5 px-10 border border-ternary-light dark:border-ternary-dark shadow-lg rounded-xl mb-8 cursor-default inset-0 transform hover:-rotate-45 hover:scale-75 transition duration-300 hover:shadow-2xl"
				/> Framework Bootstrap
			</div>
			<div>
				<img
					src="../../assets/images/brands/vuejs.png"
					alt=""
					class="w-64 py-5 px-10 border border-ternary-light dark:border-ternary-dark shadow-lg rounded-xl mb-8 cursor-default inset-0 transform hover:rotate-90 hover:scale-75 transition duration-300 hover:shadow-2xl"
				/> Framework Vuejs
			</div>
			<div>
				<img
					src="../../assets/images/brands/laravel.png"
					alt=""
					class="w-64 py-5 px-10 border border-ternary-light dark:border-ternary-dark shadow-lg rounded-xl mb-8 cursor-default inset-0 transform hover:-rotate-90 hover:scale-75 transition duration-300 hover:shadow-2xl"
				/> Framework Laravel
			</div>
			<div>
				<img
					src="../../assets/images/brands/php.png"
					alt=""
					class="w-64 py-5 px-10 border border-ternary-light dark:border-ternary-dark shadow-lg rounded-xl mb-8 cursor-default inset-0 transform hover:rotate-180 hover:scale-75 transition duration-300 hover:shadow-2xl"
				/>PHP
			</div>
			<div>
				<img
					src="../../assets/images/brands/javascript.png"
					alt=""
					class="w-64 py-5  px-10 border border-ternary-light dark:border-ternary-dark shadow-lg rounded-xl mb-8 cursor-default inset-0 transform hover:-rotate-180 hover:scale-75 transition duration-300 hover:shadow-2xl"
				/>JavaScript
			</div>
		</div>

		</transition>

		</div>
	</div>





</template>

<script>

import gsap from 'gsap'

export default {
	setup() {
		const beforeEnter = (el) => {
			console.log('before enter - set initial state')
			el.style.transform = 'translateY(-60px)'
			el.style.opacity = 0
		}
		const enter = (el, done) => {
			console.log('starting to enter - make transition')
			gsap.to(el, {
				duration: 5,
				y: 1,
				opacity: 1,
				ease: 'bounce.out',
				onComplete: done,
			})
		}
		const afterEnter = () => {
			console.log('after enter')
		}
		return { beforeEnter, enter, afterEnter}
	},
};
</script>

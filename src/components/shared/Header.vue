<template>
	<nav id="nav" class="container mx-auto">
		<div class="z-10 max-w-screen-lg xl:max-w-screen-xl block sm:flex sm:justify-between sm:items-center my-6 animate-fade-in-down">
			<div class="flex justify-between items-center">
				<div class="flex items-center">
					<i data-feather="home" class="animate-pulse w-10 sm:w-12 h-6 sm:h-6"></i>
					<router-link to="/" class="flex"> ARDHA FATIKA  </router-link>
				</div>

				<div class="sm:hidden">
					<button
						@click="isOpen = !isOpen"
						type="buttom"
						class="focus:outline-none">
						<svg
							xmlns="http://www.w3.org/2000/svg"
							viewBox="0 0 24 24"
							class="h-6 w-6 fill-current text-secondary-dark dark:text-ternary-light">
							<path
								v-if="isOpen"
								fill-rule="evenodd"
								d="M18.278 16.864a1 1 0 0 1-1.414 1.414l-4.829-4.828-4.828 4.828a1 1 0 0 1-1.414-1.414l4.828-4.829-4.828-4.828a1 1 0 0 1 1.414-1.414l4.829 4.828 4.828-4.828a1 1 0 1 1 1.414 1.414l-4.828 4.829 4.828 4.828z"
								clip-rule="evenodd">
							</path>
							<path
								v-if="!isOpen"
								fill-rule="evenodd"
								d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z">
							</path>
						</svg>
					</button>
				</div>
			</div>

			<div :class="isOpen ? 'block' : 'hidden'" class="ml-3 sm:ml-3 mt-5 sm:mt-3 sm:flex justify-center items-center space-y-5 sm:space-y-5 md:space-y-0 lg:space-y-0">
				<router-link
					to="/about"
					class="block text-center md:text-left text-lg font-medium pb-3 "
					>About</router-link>
				<router-link
					to="/projects"
					class="block text-center md:text-left text-lg font-medium pb-3 px-5"
					>Projects</router-link>
				<router-link
					to="/contact"
					class="block text-center md:text-left text-lg font-medium pb-3"
					>Contact</router-link>

				<a href="https://api.whatsapp.com/send?phone=+6285346741110&text=Hi ardha" class="flex justify-center items-center pb-5">
					<button class="md:hidden flex text-md font-medium bg-indigo-500 hover:bg-indigo-600 text-white shadow-sm rounded-lg px-5 py-2.5">Whatsapp
					</button>
				</a>
				
			</div>
			<div class="hidden sm:flex justify-between items-center flex-col md:flex-row">
				<div> <a href="https://api.whatsapp.com/send?phone=+6285346741110&text=Hi ardha">
					<button class="text-md font-medium bg-indigo-500 hover:bg-indigo-600 text-white shadow-sm rounded-lg px-5 py-2.5">Whatsapp
					</button>
					</a>
				</div>
			
			</div>
		</div>

	</nav>
</template>

<script>

import feather from 'feather-icons';

export default {
	components: {
		
	},
	data() {
		return {
			isOpen: false,
			theme: '',
			modal: false,
		};
	},

	// methods: {
	// 	showModal() {
	// 		if (this.modal) {
	// 			//stop screen scrolling
	// 			document
	// 				.getElementsByTagName('html')[0]
	// 				.classList.remove('overflow-y-hidden');
	// 			this.modal = false;
	// 		} else {
	// 			document
	// 				.getElementsByTagName('html')[0]
	// 				.classList.add('overflow-y-hidden');
	// 			this.modal = true;
	// 		}
	// 	},
	// },
	updated() {
		feather.replace();
	},
};
</script>

<style scoped>
#nav a.router-link-exact-active {
	@apply text-indigo-500;
	@apply dark:text-indigo-400;
	@apply font-medium;
}

.modal-body {
	max-height: 500px;
}
.bg-gray-800-opacity {
	background-color: #2d374850;
}
@media screen and (max-width: 768px) {
	.modal-body {
		max-height: 400px;
	}
}
.fade-up-down-enter-active {
	transition: all 0.3s ease;
}
.fade-up-down-leave-active {
	transition: all 0.3s ease;
}
.fade-up-down-enter {
	transform: translateY(10%);
	opacity: 0;
}
.fade-up-down-leave-to {
	transform: translateY(10%);
	opacity: 0;
}

.fade-enter-active {
	-webkit-transition: opacity 2s;
	transition: opacity 0.3s;
}
.fade-leave-active {
	transition: opacity 0.3s;
}

.fade-enter,
.fade-leave-to {
	opacity: 0;
}
</style>

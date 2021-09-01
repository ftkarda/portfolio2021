<template>

	<div class="bg-gray-100 mt-32">
   <div class="flex flex-col md:flex-row justify-between border-t text-gray-800 text-sm px-4 md:px-28 py-5 md:py-0">
      <div class="flex items-center font-bold text-2xl text-indigo-500 md:justify-start justify-center">Contact Me</div>
      <div class="flex items-center space-x-20 md:justify-start justify-center py-5">
         <a href="tel:+62853-4674-1110" target="__blank" class="text-gray-700 hover:text-indigo-500  dark:hover:text-indigo-400 cursor-pointer rounded-lg bg-gray-50 dark:bg-ternary-dark hover:bg-gray-100 shadow-xl p-4 ">
			Call <i data-feather="phone-forwarded" class="animate-pulse w-10 sm:w-12 h-6 sm:h-6 "></i>
		</a> 
		
         <a href="mailto:fatikaardha@gmail.com" target="__blank" class="text-gray-700 hover:text-indigo-500 dark:hover:text-indigo-400 cursor-pointer rounded-lg bg-gray-50 dark:bg-ternary-dark hover:bg-gray-100 shadow-xl p-4">
			Mail<i data-feather="send" class="animate-pulse w-10 sm:w-12 h-6 sm:h-6"></i>
		</a>
      </div>
   </div>
</div>
</template>

<script>
import feather from 'feather-icons';
export default {
	mounted() {
		feather.replace();
	},
	updated() {
		feather.replace();
	},
};
</script>

<style scoped></style>

<template>
	<!-- Banner start -->
	<section
		class="flex flex-col sm:justify-between items-center sm:flex-row md:mt-12 mt-2 sm:mt-2 pb-5 font-mono"
	>
		<div class="w-full sm:w-3/5 text-left pt-5">
			<h1
				class="text-3xl animate-bounce  sm:text-5xl text-center sm:text-left font-semibold text-indigo-500 uppercase"
			>
				Hi, I Am
			</h1>
      <p class="text-2xl sm:text-4xl text-center sm:text-left font-semibold leading-none text-gray-400">
        <span class="typed-text text-purple-500">{{ typeValue }}</span>
        <span class="cursor" :class="{'typing': typeStatus}">&nbsp;</span>
      </p>
			
		
		</div>

		<div class="w-full sm:w-4/5 text-right mt-8 sm:mt-0 order-first md:order-last ">
			
      <transition
			appear
			@before-enter="beforeEnter"
			@enter="enter"
			@after-enter="afterEnter">
      
      <img
				
				src="@/assets/images/banner.jpg"
				alt="Developer"
			/>

      </transition>
		
		</div>
	</section>
	<div class="mb-5 md:my-5">
		<a href="/CV_Ardha_Fatika.pdf" download>
                <button type="button" class='flex bg-gradient-to-r from-indigo-500 to-pink-400 hover:from-pink-500 hover:to-blue-300 focus:outline-none text-white sm:text-xs text-md md:text-xl uppercase font-bold shadow-lg rounded-full mx-auto p-3'>
                    <div class="flex sm:flex-cols gap-2">
                        <div class="col-span-1">
                            <svg xmlns="http://www.w3.org/2000/svg" class="md:h-12 md:w-12 h-9 w-9" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M15 13l-3 3m0 0l-3-3m3 3V8m0 13a9 9 0 110-18 9 9 0 010 18z" />
                            </svg>
                        </div>
                        <div class="col-span-2 flex justify-center items-center">Download CV</div>
                    </div>    
                </button>
		</a>
    </div>
	<!-- Banner end -->
</template>

<script>
import feather from 'feather-icons';
import { setTimeout } from 'timers';
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
				duration: 3,
				y: 0,
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

	name: 'Home',
	data: () => {
		return {
        typeValue: '',
        typeStatus: false,
        typeArray: ['Ardha Fatika', 'Front-end Web Developer', 'Web Design',],
        typingSpeed: 50,
        erasingSpeed: 40,
        newTextDelay: 800,
        typeArrayIndex: 0,
        charIndex: 0
      }
	},
	created() {
		setTimeout(this.typeText, this.newTextDelay + 200);
	},
	mounted() {
		feather.replace();
		this.theme = localStorage.getItem('theme') || 'light';
	},
	updated() {
		feather.replace();
	},
	methods:{
      typeText() {
        if(this.charIndex < this.typeArray[this.typeArrayIndex].length) {
          if(!this.typeStatus)
            this.typeStatus = true;

          this.typeValue += this.typeArray[this.typeArrayIndex].charAt(this.charIndex);
          this.charIndex += 1;

          setTimeout(this.typeText, this.typingSpeed);
        }
        else {
          this.typeStatus = false;
          setTimeout(this.eraseText, this.newTextDelay);
        }
      },
      eraseText() {
        if(this.charIndex > 0) {
          if(!this.typeStatus)
            this.typeStatus = true;

          this.typeValue = this.typeArray[this.typeArrayIndex].substring(0, this.charIndex - 1);
          this.charIndex -= 1;
          setTimeout(this.eraseText, this.erasingSpeed);
        }
        else {
          this.typeStatus = false;
          this.typeArrayIndex += 1;
          if(this.typeArrayIndex >= this.typeArray.length)
            this.typeArrayIndex = 0;

          setTimeout(this.typeText, this.typingSpeed + 1000);
        }
      }
    },
};
</script>

<style scoped>


</style>

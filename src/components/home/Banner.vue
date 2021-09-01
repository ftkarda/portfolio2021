<template>
	<!-- Banner start -->
	<section
		class="flex flex-col sm:justify-between items-center sm:flex-row md:mt-12 mt-2 sm:mt-2 pb-5 font-mono"
	>
		<div class="w-full sm:w-1/2 text-left pt-5">
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

<template>

    <div class="bg-gray-50 text-primary-dark md:mt-16 mt-10">
    <div class="mx-auto flex flex-col items-start md:flex-row">
    
      <div class="flex flex-col w-full sticky md:top-36 lg:w-1/3 mt-2 pt-3 sm:pt-0 md:mt-10 px-3 animate-fade-in-down">
      <img src="/profile.jpg" class="rounded-xl w-96" alt="">
        <p class="text-indigo-500 tracking-loose font-bold text-2xl text-center pt-3">Ardha Fatika, S.Kom.</p>
        <p class="text-xl leading-normal md:leading-relaxed mb-2 text-center ">Front End Developer & Web Design</p>
        <p class="text-sm text-ternary-dark mb-4 text-left">
          He is self-motivated with passion in technology & software engineering, expertise creating and design a website, dedicated on programming, eager to learn new things, easy to adapt, and able to work in a team.
        </p>
      </div>

      <div class="ml-0 md:ml-12 lg:w-2/3 sticky animate-fade-in-down">
        <div class="container mx-auto w-full h-full">
        
          <transition 
          appear 
          name="fade" 
          @before-enter="beforeEnter" 
          @enter="enter" 
          @after-enter="afterEnter" 
          @before-leave="beforeLeave" 
          @leave="leave" 
          @after-leave="afterLeave">
            <h1 
            v-if="showTitle" 
            class="mt-10 pb-5 font-bold text-2xl md:text-5xl text-center font-mono"
            >Work Experience
            </h1>
          </transition>
       
          <div class="relative wrap overflow-hidden h-full">
            <div class="border-2-2 border-indigo-500 absolute h-full border"
              style="right: 50%; border: 2px solid #6366f1; border-radius: 1%;"></div>
            <div class="border-2-2 border-indigo-500 absolute h-full border"
              style="left: 50%; border: 2px solid #6366f1; border-radius: 1%;"></div>
            <div class="mb-8 flex justify-between flex-row-reverse items-center w-full left-timeline">
              <div class="order-1 w-5/12"></div>
              <div class="order-1 w-6/12 pr-4 py-4 md:text-right text-left">
                <p class="mb-3 text-sm md:text-base text-purple-500">May 2021 - Now 2021</p>
                <p class="md:font-bold font-semibold text-lg md:text-2xl">CV KLIK IT Consultant</p>
                <p class="text-sm md:text-lg font-medium mb-3 text-gray-500">Front End Web Developer & Web Design</p>
                <p class="text-sm md:text-base leading-snug text-ternary-dark text-opacity-100">
                  Create landing page klikshop, <br> build company profile cvklik. <br>In charge of maintenance of the website cvklik, halopajajaran, and klikshop
                </p>
              </div>
            </div>
            <div class="mb-8 flex justify-between items-center w-full right-timeline">
              <div class="order-1 w-5/12"></div>
              <div class="order-1  w-6/12 pl-4 py-4 text-left">
                <p class="mb-3 text-sm md:text-base text-purple-500">May 2017 - Aug 2017</p>
                <p class="md:font-bold font-semibold text-lg md:text-2xl">Auto2000 Suci</p>
                <p class="text-sm md:text-lg font-medium mb-3 text-gray-500 ">Intern</p>
                <p class="text-sm md:text-base leading-snug text-ternary-dark text-opacity-100">
                  Create an application project such as stopwatch for time management in workshop.
                </p>
              </div>
            </div>
            <div class="mb-8 flex justify-between flex-row-reverse items-center w-full left-timeline pb-10">
              <div class="order-1 w-5/12"></div>
              <div class="order-1 w-6/12 pr-4 py-4 md:text-right text-left">
                <p class="mb-3 text-sm md:text-base text-purple-500"> May 2016 - Aug 2016</p>
                <p class="md:font-bold font-semibold text-lg md:text-2xl">Telkom Balikpapan</p>
                <p class="text-sm md:text-lg font-medium mb-3 text-gray-500">Intern</p>
                <p class="text-sm md:text-base leading-snug text-ternary-dark text-opacity-100">
                  Create, update, delete data consumer from Telkom database also migrate data consumer from speedy to indihome product.
                </p>
              </div>
            </div>

            <div class="mb-8 flex justify-between items-center w-full right-timeline">
              <div class="order-1 w-5/12"></div>

              <div class="order-1  w-5/12 px-1 py-4">
                
                <p class="md:mb-3 mb-7 font-bold text-lg md:text-2xl text-left">Work Experience</p>
                
              </div>
            </div>
          </div>
          <img class="mx-auto -mt-36 md:-mt-36" src="https://user-images.githubusercontent.com/54521023/116968861-ef21a000-acd2-11eb-95ac-a34b5b490265.png" />
        </div>
      </div>
    </div>
  </div>
</template>



<script>
import { ref } from 'vue'

export default {
	setup() {
    const showTitle = ref(true)

    const beforeEnter = (el) => {
      el.style.color = '#A5B4FC'
      console.log('before enter', el)
    }
    const enter = (el) => {
      el.style.color = '#818CF8'
      console.log('enter', el)
    }
    const afterEnter = (el) => {
      el.style.color = '#6366F1'
      console.log('after enter', el)

      setTimeout(() => showTitle.value = false, 2500)
    }

    const beforeLeave = (el) => {
      el.style.color = '#818CF8'
      console.log('before leave', el)
    }
    const leave = (el) => {
      el.style.color = '#A5B4FC'
      console.log('leave', el)
    }
    const afterLeave = (el) => {
      console.log('after leave', el)
    }

    return { showTitle, beforeEnter, enter, afterEnter, beforeLeave, leave, afterLeave }
  },
};
</script>

<style scoped>

.fade-enter-from {
  opacity: 0;
}
.fade-leave-to {
  opacity: 1;
}
.fade-enter-active {
  transition: opacity 3s ease;
}
.fade-leave-from{
  opacity: 1;
}
.fade-leave-to {
  opacity: 0;
}
.fade-leave-active {
  transition: opacity 3s ease;
}

</style>

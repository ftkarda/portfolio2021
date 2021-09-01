<template>
	<div :class="appTheme">
		<!-- Header Start -->
		<Header></Header>

		<!-- Render Active Component Contents Start -->
		<router-view v-slot="{ Component }">
			<transition name="route" mode="out-in">
				<component :is="Component"></component>
			</transition>
		</router-view>

		<!-- Footer Start -->
		<Footer></Footer>
	</div>
</template>

<script>
import feather from 'feather-icons';
import Header from './components/shared/Header';
import Footer from './components/shared/Footer';


export default {
	components: {
		Header,
		Footer,
	},
	data: () => {
		return {
			appTheme: localStorage.getItem('theme'),
		};
	},
	mounted() {
		feather.replace();
	},
	updated() {
		feather.replace();
	},
};
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
}

/* route transition */
.route-enter-from {
	opacity: 0;
	transform: translateX(100px);
}
.route-enter-active {
	transition: all 0.3s ease-out;
}
.route-leave-to {
	opacity: 0;
	transform: translateX(-100px);
}
.route-leave-active {
	transition: all 0.3s ease-in;
}

</style>

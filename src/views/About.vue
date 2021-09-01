<template>
	<div>
		<div class="container mx-auto">
			<!-- About me start -->

			<AboutMe />
			
			<!-- About me end -->
		</div>

        <div>
		<!-- About counter start -->
		<Skill />
		<!-- About counter end -->
		</div>

        <div>
        <Certificate />
        </div>

	</div>
</template>

<script>
import AboutMe from '@/components/about/AboutMe';
import Skill from '@/components/about/Skill';
import Certificate from '@/components/about/Certificate';

import feather from 'feather-icons';

export default {
	name: 'About',
	components: {
		AboutMe,
		Skill,
		Certificate,
	},
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

<style scoped></style>

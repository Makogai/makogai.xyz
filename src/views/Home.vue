<template>
	<div class="container mx-auto">
		<!-- Banner -->
		<AppBanner class="mb-5 sm:mb-8" />

		<!-- Projects -->
		<div class="soon">

		<ProjectsGrid />

		<!-- Load more projects button -->
		<div class="mt-10 sm:mt-20 flex justify-center">
			<router-link
				to="/projects"
				class="flex items-center px-6 py-3 rounded-xl shadow-lg hover:shadow-xl bg-indigo-500 hover:bg-indigo-600 focus:ring-1 focus:ring-indigo-900 text-white text-lg sm:text-xl font-medium"
				aria-label="More Projects"
				>More Projects</router-link
			>
		</div>
		<div class="flex items-center justify-center rounded-2xl soon-overlay">
					<div class="text-center">
			<p
				class="text-4xl sm:text-5xl text-shadow font-semibold mb-3 text-ternary-dark dark:text-ternary-light"
			>
				Coming soon...
			</p>
			<!-- Note: This description is commented, if you want to, you can uncomment this -->
			<!-- <p class="text-md sm:text-xl text-gray-500 dark:text-ternary-light">
				{{ projectsDescription }}
			</p> -->
		</div>
		</div>
		</div>
	</div>
</template>

<script>
import AppBanner from '@/components/AppBanner';
import ProjectsGrid from '../components/ProjectsGrid.vue';

export default {
	name: 'Home',
	components: {
		AppBanner,
		ProjectsGrid,
	},
};
</script>

<style scoped>
.soon {
	position: relative;
}
.soon-overlay {
	position: absolute;
	height: 110%;
	width: 110%;
	margin-left: -5%;
	background-color: rgba(255, 255, 255, 0.295);
	backdrop-filter: blur(6px);
	top: 0;
	left: 0;
}

  .text-shadow {
    text-shadow: 0 2px 4px rgba(0,0,0,0.50);
  }

  .text-shadow-md {
    text-shadow: 0 4px 8px rgba(0,0,0,0.12), 0 2px 4px rgba(0,0,0,0.08);
  }

  .text-shadow-lg {
    text-shadow: 0 15px 30px rgba(0,0,0,0.11), 0 5px 15px rgba(0,0,0,0.08);
  }

  .text-shadow-none {
    text-shadow: none;
  }

</style>

<template>
	<div class="container justify-center mx-auto sm:flex py-5 sm:py-10 mt-5 sm:mt-10">
		<!-- Contact form -->
		<div class="w-full sm:w-2/3 text-center items-center">
			<img
				v-if="theme === 'light'"
				src="@/assets/images/404-light.svg"
				alt="Developer"
			/>
			<img
				v-else
				src="@/assets/images/404-dark.svg"
				alt="Developer"
			/>
		</div>
	</div>
</template>

<script>
import feather from 'feather-icons';

export default {
	components: {
	},
	data: () => {
		return {
			contacts: [
				{
					id: 1,
					name: 'Your Address, Your City, Your Country',
					icon: 'map-pin',
				},
				{
					id: 2,
					name: 'email@domain.com',
					icon: 'mail',
				},
				{
					id: 3,
					name: '555 8888 888',
					icon: 'phone',
				},
			],
		};
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

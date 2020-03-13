<template>

	<v-app-bar
		app
		absolute
		hide-on-scroll
		>
		
		<v-app-bar-nav-icon></v-app-bar-nav-icon>
		
		<v-toolbar-title>Cameron Mockabee</v-toolbar-title>
		
		<v-spacer></v-spacer>


		<v-btn
			v-for="(button, i) in buttons"
			:key="i"
			:to="button.to"
			depressed
			text
			min-width="100"
			>
		
			{{button.name}}
		</v-btn>

	</v-app-bar>

</template>


<script>
	export default {
		name: 'AppBar',
		data() {
			return {
				buttons: [
					{ name: 'Home', to: '/' },
					{ name: 'About', to: '/About' },
					{ name: 'Contact', to: '/Contact' }  
				]
			}
		}
	};
</script>
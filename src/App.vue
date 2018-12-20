<template>
  <div id="app">
    <home></home>
  </div>
</template>

<script>
import Home from './components/Home.vue'
export default {
  name: 'App',
	components:{
		'home':Home
	}
}
</script>

<style>
	*{
		padding: 0;
		margin: 0;
	}
</style>

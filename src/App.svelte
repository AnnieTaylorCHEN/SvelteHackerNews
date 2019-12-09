<script>
	import { Router, Link, Route } from "svelte-routing";
	import Navigation from './components/Navigation.svelte'
	import Home from './pages/Home.svelte'
	import SingleItem from './pages/SingleItem.svelte'
	export let name;
</script>
<Router>
	<Navigation />
	<main>
		
		<h1>Hello {name}!</h1>
		<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	</main>
	<Route path="/" component={Home}></Route>
	<Route path="/item/:id" component={SingleItem}></Route>
	
</Router>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
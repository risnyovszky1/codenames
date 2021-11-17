<script>
	import { Router, Route, Link } from "svelte-navigator";

	// pages
	import Index from "./pages/Index.svelte";
	import Generator from "./pages/Generator.svelte";
	
	export let menu = 1;
</script>

<style type="text/scss">
	@import './scss/app.scss';
	
</style>

<Router>
	<header>
	  <nav>
		<Link to="/">Home</Link>
		<Link to="generator">Generator</Link>
	  </nav>
	</header>
  
	<main>
	  <Route path="/">
		<Index />
	  </Route>
  
	  <Route path="/generator">
		<Generator />
	  </Route>
  
	</main>
  </Router>
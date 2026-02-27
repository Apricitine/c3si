<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<div class="header">
	<div class="content">
    	<h1 class="info">C3 App / List of summer programs & volunteering opportunities</h1>
	</div>

	<div class="routes">
		<div class="r"><a >Home</a></div>
		<div class="r"><a class="route-link" href="./scholarships">Scholarships</a></div>
		<div class="r"><a class="route-link" href="./internships">Internships</a></div>
	</div>
</div>

{@render children()}



<style lang="scss">
	@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100..900;1,100..900&display=swap');
	
	h1.info, a {
		text-align: center;
		font-family: "Roboto", sans-serif;
		font-weight: 700;
	}

	h1 {
		color: white;

		text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
	}

	a {
		color: white;
		font-size: 25px;
		text-decoration: none;

		text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
	}

	a:hover {
		color: #F0F0F0;
	}

	div.content {
		background: linear-gradient(135deg, #E33434 0%, #F2AC2C 100%);
		width: auto;
		height: 300px;
		padding: 0 0 0 0;
		margin: 0 0 0 0;

		display: grid;
		place-items: center;
		height: 200px;
	}

	div.routes {
		width: 100%;
		display: flex;
  		justify-content: space-around;
	}

	div.r {
		width: 100%;
		border: 1px solid black;
		text-align: center;
		background-color: #DBDBDB;
		padding: 20px;
		
	}

	div.end {
		border: 1px solid black;
	}
</style>
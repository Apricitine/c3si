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
		<div class="routes">
			<a class="route-link" href="./scholarships">Scholarships</a>
			<a class="route-link" href="./internships">Internships</a>
		</div>
	</div>
</div>

{@render children()}



<style lang="scss">
	div.border {
		border: 1px solid black;
	}

	h1.info {
		text-align: center;
	}

	div.content {
		background: linear-gradient(135deg, #EF5777 0%, #5758BB 100%);
		width: auto;
		height: auto;
		padding: 20px 20px 20px 20px;
		margin: 20px 20px 20px 20px;
	}

	table {
		margin: 0 auto;
		background-color: white;
	}

	table, th, td {
		border: 1px solid black;
		border-collapse: collapse;
	}

	th, td {
		padding: 8px;
		text-align: left;
	}

	div.end {
		border: 1px solid black;
	}
</style>
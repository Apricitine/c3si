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

</style>
<script>
  let { data } = $props();
</script>

<div class="border"></div>

<div class="content">
    <h1 class="info">C3 App / List of summer programs & volunteering opportunities</h1>
    <ul>
    {#each data.scholarships as scholarship}
        <li><a href={scholarship.primary_link}>{scholarship.name}</a> - {scholarship.description}</li>
    {/each}
    </ul>
</div>

<div class="end"></div>

<p>Info</p>



<style lang="scss">
    


</style>
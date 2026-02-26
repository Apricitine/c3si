<script>
  let { data } = $props();
</script>

<div class="border"></div>



<div class="end"></div>

<ul>
{#each data.scholarships as scholarship}
    <li><a href={scholarship.primary_link}>{scholarship.name}</a> - {scholarship.description}</li>
{/each}
</ul>



<style lang="scss">
    


</style>
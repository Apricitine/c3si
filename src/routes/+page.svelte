<script>
  let { data } = $props();
</script>

<ul>
  {#each data.scholarships as scholarship}
    <li><a href={scholarship.primary_link}>{scholarship.name}</a> - {scholarship.description}</li>
  {/each}
</ul>
<script>
  let { data } = $props();
</script>

<ul>
  {#each data.scholarships as scholarship}
    <li><a href={scholarship.primary_link}>{scholarship.name}</a> - {scholarship.description}</li>
  {/each}
</ul>
	
<div class="border"></div>

<div class="content">
    <h1 class="info">C3 App / List of summer programs & volunteering opportunities</h1>

    <table>
        <tbody>
            <tr>
                <th>Name 1</th>
                <td>Description 1</td>
            </tr>
            <tr>
                <th>Name 2</th>
                <td>Description 2</td>
            </tr>
            <tr>
                <th>Name 3</th>
                <td>Description 3</td>
            </tr>
            <tr>
                <th>Name 4</th>
                <td>Description 4</td>
            </tr>
            <tr>
                <th>Name 5</th>
                <td>Description 5</td>
            </tr>
        </tbody>
    </table>
</div>

<div class="end"></div>

<p>Info</p>
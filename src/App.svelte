<script>
let name = ''
let showTable = true;
const handleNameInput=(event=>{
  name = event.target.value;
})
</script>

<main>
  {#if showTable === false}
  <p on:click={()=>showTable=!showTable} class="btn btn-primary">Show Table</p>
  {/if}
  {#if showTable}
  <p on:click={()=>showTable=!showTable} class="btn btn-primary">Hide Table</p>
  {/if}

<input bind:value={name} type="text" class="input input-secondary">
<p>My name is: {name}</p>
<hr>
 
{#if showTable}
<table class="table table-lg">
  <thead>
  <tr>
    <th class="table">Test table</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>item 1</td>
    <td>item 2</td>
    <td>itme 3</td>
  </tr>
</tbody>
</table>
{/if}
</main>



<script>
    let showTable = true;

    let devices = [{id:1, name:'Device1'},{id:2,name:'Device2'},{id:3,name:'Device3'},{id:4,name:'Device4'}]
</script>
<main>
    {#if showTable === false}
    <p on:click={()=>showTable=!showTable} class="btn btn-primary">Show Table</p>
    {/if}
    {#if showTable}
    <p on:click={()=>showTable=!showTable} class="btn btn-primary">Hide Table</p>
    {/if}
  

{#if showTable}
<table class="table table-lg">
  <thead>
  <tr>
    <th class="table">Test table</th>
  </tr>
</thead>
<tbody>
  <tr>
    {#each devices as device}
      <td>{device.name}</td>
    {/each}
    
  </tr>
</tbody>
</table>
{/if}
</main>
<script>
  import Table from "./Table.svelte";
let name = ''
/*
const handleNameInput=(event=>{
  name = event.target.value;
})
*/
</script>

<main>
<input placeholder="Input Name" bind:value={name} type="text" class="input input-secondary">
<p>My name is: {name}</p>
<hr>
<Table></Table>
</main>



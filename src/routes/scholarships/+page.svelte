<script>
    import Modal from '$lib/components/Modal.svelte';
    import Scholarship from "$lib/components/Scholarship.svelte"
    let showModal = $state(false);
    

    let { data } = $props()


</script>




{#each data.scholarships as scholarship}
    <button onclick={() => (showModal = true)}>show modal</button>
    <Scholarship name={scholarship.name} deadline={formatDate(new Date(scholarship.deadline))} description={scholarship.description}/>
{/each}

<Modal bind:showModal>
    
</Modal>

<h1>hi</h1>

<style>
    dialog {
		border-radius: 5px;
		border-width: 1px;
		transition: all 2s;
	}
</style>
<script>
    import Modal from '/src/lib/components/Modal.svelte';
    let showModal = $state(false);

</script>

<h1>hi</h1>

<button onclick={() => (showModal = true)}>show modal</button>

<Modal bing:showModal>
    <h1> hi</h1>
</Modal>

<dialog>
    <h1> hi</h1>
</dialog>

<style>
    dialog {
		border-radius: 5px;
		border-width: 1px;
		transition: all 2s;
	}
</style>
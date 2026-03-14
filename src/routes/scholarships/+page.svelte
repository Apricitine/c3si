<script lang="ts">
    import type { PageServerData } from "../$types";
    import Modal from "$lib/components/Modal.svelte"
    import Scholarship from "$lib/components/Scholarship.svelte"
    import Tag from "$lib/components/Tag.svelte"
    import Search from "$lib/components/Search.svelte"
    import stringSimilarity from "$lib/scripts/Regex"
    
    let { data }: PageServerData = $props() satisfies Scholarship[]
    let showModal = $state(false)
    let searchTerm = $state("");

    let goodData = data as Scholarship[]

    let formatDate = (date: Date) =>
        `${date.getMonth() + 1}/${date.getDate()}/${date.getFullYear()}`
    let noZero = (str: string): string => str.replace(/^0+(?!$)/, "")

    const searchSchols = () => {

    }
    

</script>

<Search bind:searchTerm on:input />
{#each data.scholarships as scholarship}
    <Scholarship onclick={() => (showModal = true)}
        name={scholarship.name}
        deadline={formatDate(new Date(scholarship.deadline))}
        description={scholarship.description}
    />
{/each}


<Modal bind:showModal>
    hi
    <Tag color="cyan" name="monkey"></Tag>
</Modal>
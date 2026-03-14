<script lang="ts">
    export let searchTerm: string
</script>

<div class="search-input-cont">
    <input type="text"
        class="search-field"
        placeholder="Enter Search Term"
        autocomplete="off"
        bind:value={searchTerm}
        on:input />
</div>


<style lang="scss">
    .search-input-cont {
        width:40%;
        display: flex;
        align-items: center;
        margin: 0 0 0 10vw;
    }

</style>
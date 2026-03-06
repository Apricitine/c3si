<script lang="ts">


    const colorHexes = {
        cyan: "#00FFFF",
        red: "#FF0000",
        green: "#008000",
        yellow: "#FFEA00",
        orange: "#FF8C00",
        purple: "#9F2B6"
    }

    type Color = keyof typeof colorHexes;

    interface Tag {
        color: Color
        name: string
    }

    let { color, name }: Tag = $props()

</script>



<div class="tag" style={`background-color: ${colorHexes[color]}`}>
    {name}
</div>


<style lang="scss">
    .tag {
        position: flex;

    }
</style>
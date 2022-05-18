<script>
export let name;
export let color;
export let ratio;
export let description;

// let formattedName = name.toLowerCase();
// let formattedColor = color.toUpperCase();
</script>

<section style="--color: {color}">
    <div 
        class="swatch"
        style="background: {color}"
    ></div>
    <div class="details">
        <h2>{name}</h2>
        <p>{color}</p>
        {#if ratio}
            <p>{ratio}</p>
        {/if}
        {#if description}
            <p>{description}</p>
        {/if}
    </div>
</section>

<style lang="scss">
    section {
        width: auto;
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        align-items: center;
        gap: 8px
    }

    .details {
        width: auto;
        flex: 1;
    }

    .swatch {
        flex: 1;
        width: 120px;
        height: 80px;
        border-radius: 3px;
        padding: 0;
        margin: 0;
    }

    h2 {
        margin: 0;
        padding: 0;
        font-size: .8rem;
        font-weight: 700;
    }

    p {
        font-size: .6rem;
        margin: 0;
        padding: 0;
        color: #999;
    }
</style>
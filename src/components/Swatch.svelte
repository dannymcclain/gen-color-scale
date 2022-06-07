<script>
export let name;
export let color;
export let ratio;
export let description;

let formattedName = name.toLowerCase();
let formattedColor = color.toUpperCase();
</script>

<section style="--color: {color}">
    <div 
        class="swatch"
        style="background: {color}"
    ></div>
    <div class="details">
        <h2>{formattedName}</h2>
        <p>{formattedColor}</p>
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
        // width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-start;
        margin-bottom: 8px;
    }

    .details {
        margin-top: .5rem;
    }

    .swatch {
        aspect-ratio: 1/1;
        width: 144px;
        border-radius: 4px;
        height: auto;
        padding: 0;
        margin: 0;
    }
    .swatch:not(last-child) {
        margin-right: 8px;
    }

    h2 {
        margin: 0;
        padding: 0;
        font-size: .92rem;
        font-weight: 700;
    }

    p {
        font-size: .75rem;
        margin: 0;
        padding: 0;
        color: #999;
    }
</style>
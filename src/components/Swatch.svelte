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
    }

    .details {
        margin-top: .5rem;
    }

    .swatch {
        width: 120px;
        height: 80px;
        padding: 0;
        margin: 0;
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
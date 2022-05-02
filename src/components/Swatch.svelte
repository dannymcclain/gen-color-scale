<script>
export let name;
export let color;
</script>

<section style="--color: {color}">
    <div 
        class="swatch"
        style="background: {color}"
    ></div>
    <div class="details">
        <h2>{name}</h2>
        <p>{color}</p>
    </div>
</section>

<style lang="scss">
    section {
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-start;
    }

    .details {
        margin-top: .5rem;
    }

    .swatch {
        aspect-ratio: 1;
        width: 100%;
        min-width: 8rem;
        height: auto;
        padding: 0;
        margin: 0;
    }

    h2 {
        margin: 0;
        padding: 0;
        font-size: 1rem;
        font-weight: 700;
    }
    p {
        font-size: .75rem;
        margin: 0;
        padding: 0;
        color: #999;
    }
</style>
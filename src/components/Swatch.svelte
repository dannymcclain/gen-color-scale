<script>
export let name;
export let color;
// export let hex;

let hex;
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
        border-radius: 8px;
        border: 1px solid #f5f5f5;
        padding: .25rem;
    }
    .details {
        padding: .5rem;
    }
    .swatch {
        aspect-ratio: 1;
        width: 100%;
        min-width: 8rem;
        height: auto;
        padding: 0;
        margin: 0;
        border-radius: 4px;
    }

    h2 {
        margin: 0;
        padding: 0;
        font-size: 1.25rem;
        // font-weight: 800;
    }
    p {
        margin: 0;
        padding: 0;
        color: #999;
    }
</style>
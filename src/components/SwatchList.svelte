<script>
    import Swatch from './Swatch.svelte'
    import tinycolor from '../tinycolor'

    function getRatio(swatch){
            let fullRatio = tinycolor.readability(swatch, '#fff');
            let ratio = Math.round((fullRatio + Number.EPSILON) * 100) / 100;
            return ratio;
        }
    
        let colorPalette = [
    { name: 'red', color: '#db351f', get ratio() { return getRatio(this.color) } },
    { name: 'navy-muted', color: '#272f46', get ratio() { return getRatio(this.color) } },
    { name: 'navy', color: '#0c1733', get ratio() { return getRatio(this.color) } },
    { name: 'white', color: '#ffffff', get ratio() { return getRatio(this.color) } },
    {
        name: "blue-lightest",
        color: "#EAF2FF",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "blue-light",
        color: "#D7E6FE",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "blue",
        color: "#3384FF",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "blue-dark",
        color: "#1559C0",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "blue-darker",
        color: "#0F4089",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "blue-accent",
        color: "#0965EF",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "grass-light",
        color: "#D5F2BE",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "grass",
        color: "#75CC32",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "grass-dark",
        color: "#44761D",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "grass-darker",
        color: "#294D0E",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "gray-light",
        color: "#E8E8E8",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "gray",
        color: "#A8A8A8",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "gray-dark",
        color: "#666666",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "gray-darker",
        color: "#444444",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "green-light",
        color: "#CAF1DC",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "green",
        color: "#02AA51",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "green-dark",
        color: "#027739",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "green-darker",
        color: "#024E26",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "green-accent",
        color: "#008940",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "mist-lightest",
        color: "#F3F5F6",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "mist-light",
        color: "#E5E8EA",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "mist",
        color: "#9DABB2",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "mist-dark",
        color: "#596A72",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "mist-darker",
        color: "#3A444A",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "orange-light",
        color: "#FFE4D1",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "orange",
        color: "#FF9347",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "orange-dark",
        color: "#A84C09",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "orange-darker",
        color: "#6E3106",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "pink-light",
        color: "#FBE3F5",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "pink",
        color: "#EF75CF",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "pink-dark",
        color: "#B32C8F",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "pink-darker",
        color: "#791A60",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "purple-light",
        color: "#F1E3FB",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "purple",
        color: "#AF5EED",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "purple-dark",
        color: "#8932CC",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "purple-darker",
        color: "#60238E",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "rose-light",
        color: "#FDE2E3",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "rose",
        color: "#EB4B51",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "rose-dark",
        color: "#C32227",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "rose-darker",
        color: "#890F13",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "rose-accent",
        color: "#E5232A",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "sky-light",
        color: "#CAEEFB",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "sky",
        color: "#05B8F9",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "sky-dark",
        color: "#036E95",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "sky-darker",
        color: "#024963",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "slate-light",
        color: "#E2E3E8",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "slate",
        color: "#9C9EAA",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "slate-dark",
        color: "#606270",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "slate-darker",
        color: "#41434D",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "teal-light",
        color: "#C9F1F1",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "teal",
        color: "#24D0D0",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "teal-dark",
        color: "#0C7272",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "teal-darker",
        color: "#054B4B",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "violet-light",
        color: "#EBE8FC",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "violet",
        color: "#8670F4",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "violet-dark",
        color: "#6148DE",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "violet-darker",
        color: "#44329E",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "yellow-light",
        color: "#FFE8B2",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "yellow",
        color: "#FFC133",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "yellow-dark",
        color: "#825D06",
        get ratio() { return getRatio(this.color) }
    },
    {
        name: "yellow-darker",
        color: "#593F01",
        get ratio() { return getRatio(this.color) }
    }
];

</script>

<style lang="scss">
    :global(*), :global(body) {
        text-align: left;
    }
    .swatches {
        width:100%;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        gap:0;
    }
    .palette {
        margin-bottom: 1.25rem;
    }
    .object {
        margin-top: 4rem;
    }

    pre {
        padding: 2rem;
        margin-top: 2rem;
        border-radius: .5rem;
        background: #f5f5f5;
        font-family: 'Menlo', monospace;
        font-size: .75rem;
        height: 20rem;
        overflow: scroll;
    }
</style>

<section class="swatches">
    {#each colorPalette as {name, color, ratio}}
        <Swatch {name} {color} {ratio} />
    {/each}
</section>

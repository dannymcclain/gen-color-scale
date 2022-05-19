<script>
    import Swatch from './Swatch.svelte'
    import tinycolor from '../tinycolor'

    function getRatio(swatch){
            let fullRatio = tinycolor.readability(swatch, '#fff');
            let ratio = Math.round((fullRatio + Number.EPSILON) * 100) / 100;
            return ratio;
    }
    
    let colorPalette = [
        { swatch: 'built', colors:
            [
                {name: 'built-navy', color: '#0c1733', get ratio() { return getRatio(this.color)}},
                {name: 'built-navy-muted', color: '#272f46', get ratio() { return getRatio(this.color)}},
                {name: 'built-white', color: '#ffffff', get ratio() { return getRatio(this.color)}},
                {name: 'built-red', color: '#db351f', get ratio() { return getRatio(this.color)}},
                
            ]
        },
        {swatch: 'rose', colors: [
            { name: 'rose-50', color: '#FEF0F1', get ratio() { return getRatio(this.color)} },
            { name: 'rose-100', color: '#FDE2E3', get ratio() { return getRatio(this.color)} },
            { name: 'rose-500', color: '#EF4C52', get ratio() { return getRatio(this.color)} },
            { name: 'rose-600', color: '#DF2A30', get ratio() { return getRatio(this.color)} },
            { name: 'rose-700', color: '#C32227', get ratio() { return getRatio(this.color)} },
            { name: 'rose-800', color: '#890F13', get ratio() { return getRatio(this.color)} },
        ]},
        {swatch: 'orange', colors: [
            { name: 'orange-50', color: '#FFF3EA', get ratio() { return getRatio(this.color)} },
            { name: 'orange-100', color: '#FFE4D1', get ratio() { return getRatio(this.color)} },
            { name: 'orange-500', color: '#EF6C0F', get ratio() { return getRatio(this.color)} },
            { name: 'orange-600', color: '#C0560B', get ratio() { return getRatio(this.color)} },
            { name: 'orange-700', color: '#A84C09', get ratio() { return getRatio(this.color)} },
            { name: 'orange-800', color: '#6E3106', get ratio() { return getRatio(this.color)} },
        ]},
        {swatch: 'yellow', colors: [
            { name: 'yellow-50', color: '#FFF2D6', get ratio() { return getRatio(this.color)} },
            { name: 'yellow-100', color: '#FFE8B2', get ratio() { return getRatio(this.color)} },
            { name: 'yellow-500', color: '#C18A0A', get ratio() { return getRatio(this.color)} },
            { name: 'yellow-600', color: '#9A6D03', get ratio() { return getRatio(this.color)} },
            { name: 'yellow-700', color: '#825D06', get ratio() { return getRatio(this.color)} },
            { name: 'yellow-800', color: '#593F01', get ratio() { return getRatio(this.color)} }
        ]},
        {swatch: 'grass', colors: [
            { name: 'grass-50', color: '#E8F8DC', get ratio() { return getRatio(this.color)} },
            { name: 'grass-100', color: '#D5F2BE', get ratio() { return getRatio(this.color)} },
            { name: 'grass-500', color: '#5DA625', get ratio() { return getRatio(this.color)} },
            { name: 'grass-600', color: '#4A841F', get ratio() { return getRatio(this.color)} },
            { name: 'grass-700', color: '#44761D', get ratio() { return getRatio(this.color)} },
            { name: 'grass-800', color: '#294D0E', get ratio() { return getRatio(this.color)} },
        ]},
        {swatch: 'green', colors: [
            { name: 'green-50', color: '#E6F8EF', get ratio() { return getRatio(this.color)} },
            { name: 'green-100', color: '#CAF1DC', get ratio() { return getRatio(this.color)} },
            { name: 'green-500', color: '#02AA51', get ratio() { return getRatio(this.color)} },
            { name: 'green-600', color: '#008940', get ratio() { return getRatio(this.color)} },
            { name: 'green-700', color: '#027739', get ratio() { return getRatio(this.color)} },
            { name: 'green-800', color: '#024E26', get ratio() { return getRatio(this.color)} },
        ]},
        {swatch: 'teal', colors: [
            { name: 'teal-50', color: '#E2F7F7', get ratio() { return getRatio(this.color)} },
            { name: 'teal-100', color: '#C9F1F1', get ratio() { return getRatio(this.color)} },
            { name: 'teal-500', color: '#12A5A5', get ratio() { return getRatio(this.color)} },
            { name: 'teal-600', color: '#0C8181', get ratio() { return getRatio(this.color)} },
            { name: 'teal-700', color: '#0C7272', get ratio() { return getRatio(this.color)} },
            { name: 'teal-800', color: '#054B4B', get ratio() { return getRatio(this.color)} },
        ]},
        {swatch: 'sky', colors: [
            { name: 'sky-50', color: '#E2F5FD', get ratio() { return getRatio(this.color)} },
            { name: 'sky-100', color: '#CAEEFB', get ratio() { return getRatio(this.color)} },
            { name: 'sky-500', color: '#039FD8', get ratio() { return getRatio(this.color)} },
            { name: 'sky-600', color: '#037DA9', get ratio() { return getRatio(this.color)} },
            { name: 'sky-700', color: '#036E95', get ratio() { return getRatio(this.color)} },
            { name: 'sky-800', color: '#024963', get ratio() { return getRatio(this.color)} },
            ]},
        {swatch: 'blue', colors: [
            { name: 'blue-50', color: '#EAF2FF', get ratio() { return getRatio(this.color)} },
            { name: 'blue-100', color: '#D7E6FE', get ratio() { return getRatio(this.color)} },
            { name: 'blue-500', color: '#3384FF', get ratio() { return getRatio(this.color)} },
            { name: 'blue-600', color: '#0C66ED', get ratio() { return getRatio(this.color)} },
            { name: 'blue-700', color: '#155CC5', get ratio() { return getRatio(this.color)} },
            { name: 'blue-800', color: '#0F4089', get ratio() { return getRatio(this.color)} },
        ]},
        {swatch: 'violet', colors: [
            { name: 'violet-50', color: '#F3F1FD', get ratio() { return getRatio(this.color)} },
            { name: 'violet-100', color: '#EBE8FC', get ratio() { return getRatio(this.color)} },
            { name: 'violet-500', color: '#9381ED', get ratio() { return getRatio(this.color)} },
            { name: 'violet-600', color: '#755FE1', get ratio() { return getRatio(this.color)} },
            { name: 'violet-700', color: '#6148DE', get ratio() { return getRatio(this.color)} },
            { name: 'violet-800', color: '#44329E', get ratio() { return getRatio(this.color)} },
        ]},
        {swatch: 'purple', colors: [
            { name: 'purple-50', color: '#F8F1FD', get ratio() { return getRatio(this.color)} },
            { name: 'purple-100', color: '#F1E3FB', get ratio() { return getRatio(this.color)} },
            { name: 'purple-500', color: '#B773EC', get ratio() { return getRatio(this.color)} },
            { name: 'purple-600', color: '#9C53D4', get ratio() { return getRatio(this.color)} },
            { name: 'purple-700', color: '#8E3BCE', get ratio() { return getRatio(this.color)} },
            { name: 'purple-800', color: '#60238E', get ratio() { return getRatio(this.color)} },
        ]},
        {swatch: 'pink', colors: [
            { name: 'pink-50', color: '#FDF1FA', get ratio() { return getRatio(this.color)} },
            { name: 'pink-100', color: '#FBE3F5', get ratio() { return getRatio(this.color)} },
            { name: 'pink-500', color: '#EB5AC5', get ratio() { return getRatio(this.color)} },
            { name: 'pink-600', color: '#C83CA2', get ratio() { return getRatio(this.color)} },
            { name: 'pink-700', color: '#B32C8F', get ratio() { return getRatio(this.color)} },
            { name: 'pink-800', color: '#791A60', get ratio() { return getRatio(this.color)} },
            ]},
        {swatch: 'gray', colors: [
            { name: 'gray-50', color: '#F4F4F4', get ratio() { return getRatio(this.color)} },
            { name: 'gray-100', color: '#E8E8E8', get ratio() { return getRatio(this.color)} },
            { name: 'gray-500', color: '#939393', get ratio() { return getRatio(this.color)} },
            { name: 'gray-600', color: '#757575', get ratio() { return getRatio(this.color)} },
            { name: 'gray-700', color: '#666666', get ratio() { return getRatio(this.color)} },
            { name: 'gray-800', color: '#444444', get ratio() { return getRatio(this.color)} },
        ]},
        {swatch: 'slate', colors: [
            { name: 'slate-50', color: '#F3F3F6', get ratio() { return getRatio(this.color)} },
            { name: 'slate-100', color: '#E2E3E8', get ratio() { return getRatio(this.color)} },
            { name: 'slate-500', color: '#9093A1', get ratio() { return getRatio(this.color)} },
            { name: 'slate-600', color: '#717484', get ratio() { return getRatio(this.color)} },
            { name: 'slate-700', color: '#606270', get ratio() { return getRatio(this.color)} },
            { name: 'slate-800', color: '#41434D', get ratio() { return getRatio(this.color)} },
        ]},
        {swatch: 'mist', colors: [
            { name: 'mist-50', color: '#F4F5F6', get ratio() { return getRatio(this.color)} },
            { name: 'mist-100', color: '#E5E8EA', get ratio() { return getRatio(this.color)} },
            { name: 'mist-500', color: '#84959E', get ratio() { return getRatio(this.color)} },
            { name: 'mist-600', color: '#697981', get ratio() { return getRatio(this.color)} },
            { name: 'mist-700', color: '#596A72', get ratio() { return getRatio(this.color)} },
            { name: 'mist-800', color: '#3A444A', get ratio() { return getRatio(this.color)} },
            ]},
    ];


    let stringColorScale;
    function formatPalette() {
        let formattedPalette = JSON.parse(JSON.stringify(colorPalette));
        formattedPalette.forEach(item => {
            let name = item.swatch;
            let colors = item.colors;
            colors.forEach(color => {
                color['description'] = color['ratio'];
                color.description = color.color + ', ' + color.ratio.toString();
            })
        });
        stringColorScale = JSON.stringify(formattedPalette, null, 4);
    }
    formatPalette();

    function updateClipboard(newClip) {
            navigator.clipboard.writeText(newClip).then(function() {
                /* clipboard successfully set */
                console.log('Copied!')
        }, function() {
                /* clipboard write failed */
                console.log('Failed.')
            });
    }
</script>

<style lang="scss">
    :global(*), :global(body) {
        text-align: left;
    }
    .swatches {
        display: flex;
        flex-direction: row;
        flex-wrap: nowrap;
        // gap:.5rem;
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

{#each colorPalette as swatch}
    <div class="palette">
        <section class="swatches">
            {#each swatch.colors as {name, color, ratio}}
                <Swatch {name} {color} {ratio} />
            {/each}
        </section>
    </div>
{/each}

<section class="object">
    <h2>Color Palette</h2>
    <!-- <p>A reformatted object of the color scale to use with the Figma plugin I made.</p> -->
    <button on:click={() => updateClipboard(stringColorScale)}>Copy</button>
    <pre>{stringColorScale}</pre>
</section>
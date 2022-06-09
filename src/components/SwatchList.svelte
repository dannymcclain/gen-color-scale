<script>
    import Swatch from './Swatch.svelte'
    import tinycolor from '../tinycolor'

    function getRatio(swatch){
            let fullRatio = tinycolor.readability(swatch, '#fff');
            let ratio = Math.round((fullRatio + Number.EPSILON) * 100) / 100;
            return ratio;
    }
    
    let colorPalette = [
{ swatch: 'built', colors: [
    { name: 'built-navy', color: '#0c1733', get ratio() { return getRatio(this.color)} },
    { name: 'built-navy-muted', color: '#272f46', get ratio() { return getRatio(this.color)} },
    { name: 'built-white', color: '#ffffff', get ratio() { return getRatio(this.color)} },
    { name: 'built-red', color: '#db351f', get ratio() { return getRatio(this.color)} }]},
{ swatch: 'rose', colors: [
    { name: 'rose-50', color: '#FEF1F1', get ratio() { return getRatio(this.color)} },
    { name: 'rose-100', color: '#FDE2E3', get ratio() { return getRatio(this.color)} },
    { name: 'rose-300', color: '#F2B6B8', get ratio() { return getRatio(this.color)} },
    { name: 'rose-400', color: '#F49093', get ratio() { return getRatio(this.color)} },
    { name: 'rose-500', color: '#EF4D52', get ratio() { return getRatio(this.color)} },
    { name: 'rose-600', color: '#DF2A30', get ratio() { return getRatio(this.color)} },
    { name: 'rose-700', color: '#C32228', get ratio() { return getRatio(this.color)} },
    { name: 'rose-800', color: '#8A0F14', get ratio() { return getRatio(this.color)} }]},
{ swatch: 'orange', colors: [
    { name: 'orange-50', color: '#FFF3EB', get ratio() { return getRatio(this.color)} },
    { name: 'orange-100', color: '#FFE4D1', get ratio() { return getRatio(this.color)} },
    { name: 'orange-300', color: '#FAB585', get ratio() { return getRatio(this.color)} },
    { name: 'orange-400', color: '#FA9247', get ratio() { return getRatio(this.color)} },
    { name: 'orange-500', color: '#F06D0F', get ratio() { return getRatio(this.color)} },
    { name: 'orange-600', color: '#C1570B', get ratio() { return getRatio(this.color)} },
    { name: 'orange-700', color: '#A94C0A', get ratio() { return getRatio(this.color)} },
    { name: 'orange-800', color: '#6F3206', get ratio() { return getRatio(this.color)} }]},
{ swatch: 'yellow', colors: [
    { name: 'yellow-50', color: '#FFF3D6', get ratio() { return getRatio(this.color)} },
    { name: 'yellow-100', color: '#FFE8B3', get ratio() { return getRatio(this.color)} },
    { name: 'yellow-300', color: '#EBBD52', get ratio() { return getRatio(this.color)} },
    { name: 'yellow-400', color: '#E1A20E', get ratio() { return getRatio(this.color)} },
    { name: 'yellow-500', color: '#C28B0A', get ratio() { return getRatio(this.color)} },
    { name: 'yellow-600', color: '#9A6D04', get ratio() { return getRatio(this.color)} },
    { name: 'yellow-700', color: '#835E07', get ratio() { return getRatio(this.color)} },
    { name: 'yellow-800', color: '#5A4002', get ratio() { return getRatio(this.color)} }]},
{ swatch: 'grass', colors: [
    { name: 'grass-50', color: '#E9F8DD', get ratio() { return getRatio(this.color)} },
    { name: 'grass-100', color: '#D5F3BF', get ratio() { return getRatio(this.color)} },
    { name: 'grass-300', color: '#9DD473', get ratio() { return getRatio(this.color)} },
    { name: 'grass-400', color: '#74C039', get ratio() { return getRatio(this.color)} },
    { name: 'grass-500', color: '#5DA626', get ratio() { return getRatio(this.color)} },
    { name: 'grass-600', color: '#4B841F', get ratio() { return getRatio(this.color)} },
    { name: 'grass-700', color: '#44761E', get ratio() { return getRatio(this.color)} },
    { name: 'grass-800', color: '#2A4D0F', get ratio() { return getRatio(this.color)} }]},    
{ swatch: 'green', colors: [
    { name: 'green-50', color: '#E7F9EF', get ratio() { return getRatio(this.color)} },
    { name: 'green-100', color: '#CBF1DD', get ratio() { return getRatio(this.color)} },
    { name: 'green-300', color: '#7DD8A8', get ratio() { return getRatio(this.color)} },
    { name: 'green-400', color: '#34C578', get ratio() { return getRatio(this.color)} },
    { name: 'green-500', color: '#03AB51', get ratio() { return getRatio(this.color)} },
    { name: 'green-600', color: '#018940', get ratio() { return getRatio(this.color)} },
    { name: 'green-700', color: '#027839', get ratio() { return getRatio(this.color)} },
    { name: 'green-800', color: '#034F26', get ratio() { return getRatio(this.color)} }]},
{ swatch: 'teal', colors: [
    { name: 'teal-50', color: '#E2F8F8', get ratio() { return getRatio(this.color)} },
    { name: 'teal-100', color: '#CAF2F2', get ratio() { return getRatio(this.color)} },
    { name: 'teal-300', color: '#68D4D4', get ratio() { return getRatio(this.color)} },
    { name: 'teal-400', color: '#1BC0C0', get ratio() { return getRatio(this.color)} },
    { name: 'teal-500', color: '#12A5A5', get ratio() { return getRatio(this.color)} },
    { name: 'teal-600', color: '#0D8282', get ratio() { return getRatio(this.color)} },
    { name: 'teal-700', color: '#0D7373', get ratio() { return getRatio(this.color)} },
    { name: 'teal-800', color: '#064C4C', get ratio() { return getRatio(this.color)} }]},
{ swatch: 'sky', colors: [
    { name: 'sky-50', color: '#E2F6FD', get ratio() { return getRatio(this.color)} },
    { name: 'sky-100', color: '#CAEEFC', get ratio() { return getRatio(this.color)} },
    { name: 'sky-300', color: '#7BD0EF', get ratio() { return getRatio(this.color)} },
    { name: 'sky-400', color: '#20BBF3', get ratio() { return getRatio(this.color)} },
    { name: 'sky-500', color: '#039FD8', get ratio() { return getRatio(this.color)} },
    { name: 'sky-600', color: '#037EAA', get ratio() { return getRatio(this.color)} },
    { name: 'sky-700', color: '#036F96', get ratio() { return getRatio(this.color)} },
    { name: 'sky-800', color: '#024A64', get ratio() { return getRatio(this.color)} }]},
{ swatch: 'blue', colors: [
    { name: 'blue-50', color: '#EBF3FF', get ratio() { return getRatio(this.color)} },
    { name: 'blue-100', color: '#D7E7FE', get ratio() { return getRatio(this.color)} },
    { name: 'blue-300', color: '#A3C8FF', get ratio() { return getRatio(this.color)} },
    { name: 'blue-400', color: '#7AAFFF', get ratio() { return getRatio(this.color)} },
    { name: 'blue-500', color: '#3385FF', get ratio() { return getRatio(this.color)} },
    { name: 'blue-600', color: '#0C66ED', get ratio() { return getRatio(this.color)} },
    { name: 'blue-700', color: '#165CC5', get ratio() { return getRatio(this.color)} },
    { name: 'blue-800', color: '#0F408A', get ratio() { return getRatio(this.color)} }]},    
{ swatch: 'violet', colors: [
    { name: 'violet-50', color: '#F3F1FD', get ratio() { return getRatio(this.color)} },
    { name: 'violet-100', color: '#EBE8FC', get ratio() { return getRatio(this.color)} },
    { name: 'violet-300', color: '#C7BFF3', get ratio() { return getRatio(this.color)} },
    { name: 'violet-400', color: '#B0A4EF', get ratio() { return getRatio(this.color)} },
    { name: 'violet-500', color: '#9381EE', get ratio() { return getRatio(this.color)} },
    { name: 'violet-600', color: '#7560E2', get ratio() { return getRatio(this.color)} },
    { name: 'violet-700', color: '#6249DF', get ratio() { return getRatio(this.color)} },
    { name: 'violet-800', color: '#44329F', get ratio() { return getRatio(this.color)} }]},    
{ swatch: 'purple', colors: [
    { name: 'purple-50', color: '#F8F1FD', get ratio() { return getRatio(this.color)} },
    { name: 'purple-100', color: '#F1E3FC', get ratio() { return getRatio(this.color)} },
    { name: 'purple-300', color: '#DAB9F4', get ratio() { return getRatio(this.color)} },
    { name: 'purple-400', color: '#CA9AEF', get ratio() { return getRatio(this.color)} },
    { name: 'purple-500', color: '#B874EC', get ratio() { return getRatio(this.color)} },
    { name: 'purple-600', color: '#9C54D4', get ratio() { return getRatio(this.color)} },
    { name: 'purple-700', color: '#8E3BCE', get ratio() { return getRatio(this.color)} },
    { name: 'purple-800', color: '#60248F', get ratio() { return getRatio(this.color)} }]},    
{ swatch: 'pink', colors: [
    { name: 'pink-50', color: '#FDF1FA', get ratio() { return getRatio(this.color)} },
    { name: 'pink-100', color: '#FCE3F5', get ratio() { return getRatio(this.color)} },
    { name: 'pink-300', color: '#F2B1E0', get ratio() { return getRatio(this.color)} },
    { name: 'pink-400', color: '#EE8CD3', get ratio() { return getRatio(this.color)} },
    { name: 'pink-500', color: '#EC5BC5', get ratio() { return getRatio(this.color)} },
    { name: 'pink-600', color: '#C83CA3', get ratio() { return getRatio(this.color)} },
    { name: 'pink-700', color: '#B42D90', get ratio() { return getRatio(this.color)} },
    { name: 'pink-800', color: '#791B60', get ratio() { return getRatio(this.color)} }]},
{ swatch: 'gray', colors: [
        { name: 'gray-50', color: '#F5F5F5', get ratio() { return getRatio(this.color)} },
        { name: 'gray-100', color: '#E8E8E8', get ratio() { return getRatio(this.color)} },
        { name: 'gray-300', color: '#C4C4C4', get ratio() { return getRatio(this.color)} },
        { name: 'gray-400', color: '#ADADAD', get ratio() { return getRatio(this.color)} },
        { name: 'gray-500', color: '#949494', get ratio() { return getRatio(this.color)} },
        { name: 'gray-600', color: '#757575', get ratio() { return getRatio(this.color)} },
        { name: 'gray-700', color: '#666666', get ratio() { return getRatio(this.color)} },
        { name: 'gray-800', color: '#454545', get ratio() { return getRatio(this.color)} }]},
{ swatch: 'stone', colors: [
    { name: 'stone-50',  color: '#F4F5F6', get ratio() { return getRatio(this.color)} },
    { name: 'stone-100', color: '#E5E8EB', get ratio() { return getRatio(this.color)} },
    { name: 'stone-300', color: '#C0C7CE', get ratio() { return getRatio(this.color)} },
    { name: 'stone-400', color: '#A6AFB9', get ratio() { return getRatio(this.color)} },
    { name: 'stone-500', color: '#8A96A3', get ratio() { return getRatio(this.color)} },
    { name: 'stone-600', color: '#6C7784', get ratio() { return getRatio(this.color)} },
    { name: 'stone-700', color: '#5E6873', get ratio() { return getRatio(this.color)} },
    { name: 'stone-800', color: '#3E444C', get ratio() { return getRatio(this.color)} }]},    
{ swatch: 'divider', colors: [
    { name: '', color: '', ratio: '' },
    { name: '', color: '', ratio: '' },
    { name: '', color: '', ratio: '' },
    { name: '', color: '', ratio: '' },
    { name: '', color: '', ratio: '' },
    { name: '', color: '', ratio: '' },
    { name: '', color: '', ratio: '' },
    { name: '', color: '', ratio: '' }]},    
{ swatch: 'slate', colors: [
    { name: 'slate-50', color: '#F4F4F6', get ratio() { return getRatio(this.color)} },
    { name: 'slate-100', color: '#E2E3E9', get ratio() { return getRatio(this.color)} },
    { name: 'slate-300', color: '#C2C4CB', get ratio() { return getRatio(this.color)} },
    { name: 'slate-400', color: '#AAACB6', get ratio() { return getRatio(this.color)} },
    { name: 'slate-500', color: '#9194A1', get ratio() { return getRatio(this.color)} },
    { name: 'slate-600', color: '#717484', get ratio() { return getRatio(this.color)} },
    { name: 'slate-700', color: '#606371', get ratio() { return getRatio(this.color)} },
    { name: 'slate-800', color: '#42444D', get ratio() { return getRatio(this.color)} }]},
    { swatch: 'mist', colors: [
    { name: 'mist-50', color: '#F4F5F6', get ratio() { return getRatio(this.color)} },
    { name: 'mist-100', color: '#E5E9EB', get ratio() { return getRatio(this.color)} },
    { name: 'mist-300', color: '#BEC6CA', get ratio() { return getRatio(this.color)} },
    { name: 'mist-400', color: '#A5B0B6', get ratio() { return getRatio(this.color)} },
    { name: 'mist-500', color: '#84969F', get ratio() { return getRatio(this.color)} },
    { name: 'mist-600', color: '#6A7981', get ratio() { return getRatio(this.color)} },
    { name: 'mist-700', color: '#5A6A72', get ratio() { return getRatio(this.color)} },
    { name: 'mist-800', color: '#3A454A', get ratio() { return getRatio(this.color)} }]}  
];


    let stringColorScale;
    function formatPalette() {
        let formattedPalette = JSON.parse(JSON.stringify(colorPalette));
        formattedPalette.forEach(item => {
            let name = item.swatch;
            let colors = item.colors;
            colors.forEach(color => {
                color.hex = color.color;
                color.ratio = color.ratio.toString();
                // color['description'] = color['ratio'];
                // color.description = 'Hex: ' + color.color + ', Contrast: ' + color.ratio.toString();
                // delete color['ratio'];
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
        flex-wrap: wrap;
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
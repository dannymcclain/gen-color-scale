<script>
    import Swatch from './Swatch.svelte'
    import tinycolor from '../tinycolor'

    let palette = [
        { swatch: 'Red', colors: 
            [
                {name: '900', color: '#290306'},
                {name: '800', color: '#5E0C12'},
                {name: '700', color: '#941C24'},
                {name: '600', color: '#C0323B'},
                {name: '500', color: '#e44e58'},
                {name: '400', color: '#F3646E'},
                {name: '300', color: '#FD7E87'},
                {name: '200', color: '#FF9DA4'},
                {name: '100', color: '#FFC0C5'},
                {name: '050', color: '#FFE7E9'},
            ]
            },
        { swatch: 'Orange', colors: 
            [
                {name: '900', color: '#291704'},
                {name: '800', color: '#5E3710'},
                {name: '700', color: '#945722'},
                {name: '600', color: '#CA783B'},
                {name: '500', color: '#f69b5a'},
                {name: '400', color: '#FFAB6E'},
                {name: '300', color: '#FFBC85'},
                {name: '200', color: '#FFCEA2'},
                {name: '100', color: '#FFE1C3'},
                {name: '050', color: '#FFF4E8'},
            ]
            },
        { swatch: 'Yellow', colors: [
            {name: '900', color: '#292202'},
            {name: '800', color: '#5E4C0B'},
            {name: '700', color: '#94741A'},
            {name: '600', color: '#CA9931'},
            {name: '500', color: '#f8bd4f'},
            {name: '400', color: '#FFCC64'},
            {name: '300', color: '#FFDA7D'},
            {name: '200', color: '#FFE69B'},
            {name: '100', color: '#FFF1BF'},
            {name: '050', color: '#FFFAE7'},
        ]
        },
        { swatch: 'Grass', colors: [
            {name: '900', color: '#112900'},
            {name: '800', color: '#285D00'},
            {name: '700', color: '#408806'},
            {name: '600', color: '#59AD15'},
            {name: '500', color: '#72cb2a'},
            {name: '400', color: '#8ADF46'},
            {name: '300', color: '#A3EE66'},
            {name: '200', color: '#BCF98B'},
            {name: '100', color: '#D6FFB8'},
            {name: '050', color: '#F0FFE6'},
        ]
        },
        { swatch: 'Green', colors: [
            {name: '900', color: '#00240E'},
            {name: '800', color: '#004E20'},
            {name: '700', color: '#007231'},
            {name: '600', color: '#008E43'},
            {name: '500', color: '#05a455'},
            {name: '400', color: '#2EBF74'},
            {name: '300', color: '#5CD592'},
            {name: '200', color: '#8AE7B1'},
            {name: '100', color: '#B8F4D0'},
            {name: '050', color: '#E6FCEE'},
        ]
        },
        { swatch: 'Teal', colors: [
            {name: '900', color: '#0C2728'},
            {name: '800', color: '#1F575A'},
            {name: '700', color: '#378487'},
            {name: '600', color: '#52ACB0'},
            {name: '500', color: '#72d1d5'},
            {name: '400', color: '#85DFE3'},
            {name: '300', color: '#9BEBEE'},
            {name: '200', color: '#B3F4F7'},
            {name: '100', color: '#CFFAFC'},
            {name: '050', color: '#EDFEFF'},
        ]
        },
        { swatch: 'Cyan', colors: [
            {name: '900', color: '#002729'},
            {name: '800', color: '#07565E'},
            {name: '700', color: '#158294'},
            {name: '600', color: '#2AA9CA'},
            {name: '500', color: '#47cdf5'},
            {name: '400', color: '#5DDCFF'},
            {name: '300', color: '#77E9FF'},
            {name: '200', color: '#97F2FF'},
            {name: '100', color: '#BCF9FF'},
            {name: '050', color: '#E6FEFF'},
        ]
        },
        { swatch: 'Blue', colors: [
            {name: '900', color: '#001829'},
            {name: '800', color: '#06375E'},
            {name: '700', color: '#145794'},
            {name: '600', color: '#2A78CA'},
            {name: '500', color: '#479aff'},
            {name: '400', color: '#5CABFF'},
            {name: '300', color: '#76BDFF'},
            {name: '200', color: '#96CFFF'},
            {name: '100', color: '#BBE1FF'},
            {name: '050', color: '#E6F4FF'},
        ]
        },
        { swatch: 'Violet', colors: [
            {name: '900', color: '#120C29'},
            {name: '800', color: '#2E215E'},
            {name: '700', color: '#4D3C94'},
            {name: '600', color: '#6F5BCA'},
            {name: '500', color: '#9580ff'},
            {name: '400', color: '#A38FFF'},
            {name: '300', color: '#B3A1FF'},
            {name: '200', color: '#C5B7FF'},
            {name: '100', color: '#DAD0FF'},
            {name: '050', color: '#F1EDFF'},
        ]
        },
        { swatch: 'Purple', colors: [
                {name: '900', color: '#1F0C29'},
                {name: '800', color: '#47215E'},
                {name: '700', color: '#6F3C94'},
                {name: '600', color: '#975BCA'},
                {name: '500', color: '#bf80ff'},
                {name: '400', color: '#CB8FFF'},
                {name: '300', color: '#D6A1FF'},
                {name: '200', color: '#E1B7FF'},
                {name: '100', color: '#EDD0FF'},
                {name: '050', color: '#F9EDFF'},
            ]
        },
    { swatch: 'Pink', colors: 
            [
                {name: '900', color: '#290F24'},
                {name: '800', color: '#5E2652'},
                {name: '700', color: '#8E417D'},
                {name: '600', color: '#BA60A6'},
                {name: '500', color: '#e283cd'},
                {name: '400', color: '#EE93DA'},
                {name: '300', color: '#F6A6E4'},
                {name: '200', color: '#FCBCEE'},
                {name: '100', color: '#FFD4F6'},
                {name: '050', color: '#FFEFFC'},
            ]
        },
    { swatch: 'Gray', colors: 
            [
                {name: '900', color: '#1D1D1D'},
                {name: '800', color: '#424242'},
                {name: '700', color: '#686868'},
                {name: '600', color: '#8D8D8D'},
                {name: '500', color: '#b3b3b3'},
                {name: '400', color: '#C1C1C1'},
                {name: '300', color: '#CECECE'},
                {name: '200', color: '#DCDCDC'},
                {name: '100', color: '#EAEAEA'},
                {name: '050', color: '#F7F7F7'},
            ]
        },
    { swatch: 'Slate', colors: 
            [
                {name: '900', color: '#18191C'},
                {name: '800', color: '#393940'},
                {name: '700', color: '#5A5A64'},
                {name: '600', color: '#7B7C87'},
                {name: '500', color: '#9d9eaa'},
                {name: '400', color: '#AEAFBA'},
                {name: '300', color: '#BFC0CA'},
                {name: '200', color: '#D1D1D9'},
                {name: '100', color: '#E2E3E8'},
                {name: '050', color: '#F5F5F7'},
            ]
        },
    { swatch: 'Mist', colors: 
            [
                {name: '900', color: '#191E20'},
                {name: '800', color: '#3B4549'},
                {name: '700', color: '#5D6B72'},
                {name: '600', color: '#819199'},
                {name: '500', color: '#a6b7bf'},
                {name: '400', color: '#B4C5CC'},
                {name: '300', color: '#C4D2D9'},
                {name: '200', color: '#D3DFE4'},
                {name: '100', color: '#E4ECEF'},
                {name: '050', color: '#F5F8FA'},
            ]
        },
       
        ];
</script>

<style lang="scss">
    :global(*), :global(body) {
        text-align: left;
    }
    section {
        display: flex;
        flex-direction: row;
        gap:.5rem;
    }
    div {
        margin-bottom: 1.25rem;
    }
</style>

{#each palette as swatch}
    <div>
        <!-- <h1>{swatch.swatch}</h1> -->
        <section>
            {#each swatch.colors.reverse() as {name, color}}
                <Swatch name="{swatch.swatch}-{name}" color={color} />
            {/each}
        </section>
    </div>
{/each}
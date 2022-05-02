<script>
    import Swatch from './Swatch.svelte'

    let palette = [
        { swatch: 'Red', colors: 
            [
                {name: '900', color: '#330407'},
                {name: '800', color: '#660D14'},
                {name: '700', color: '#991D25'},
                {name: '600', color: '#C2323C'},
                {name: '500', color: '#e44e58'},
                {name: '400', color: '#F1616B'},
                {name: '300', color: '#FA7880'},
                {name: '200', color: '#FF9199'},
                {name: '100', color: '#FFAEB4'},
                {name: '050', color: '#FFCED1'},
                {name: '025', color: '#FFF1F2'},
            ]
            },
        { swatch: 'Orange', colors: 
            [
                {name: '900', color: '#331D06'},
                {name: '800', color: '#663B11'},
                {name: '700', color: '#995A23'},
                {name: '600', color: '#CC7A3C'},
                {name: '500', color: '#f69b5a'},
                {name: '400', color: '#FFA96B'},
                {name: '300', color: '#FFB87F'},
                {name: '200', color: '#FFC797'},
                {name: '100', color: '#FFD7B2'},
                {name: '050', color: '#FFE8D0'},
                {name: '025', color: '#FFF8F1'},
            ]
            },
        { swatch: 'Yellow', colors: [
            {name: '900', color: '#332A02'},
            {name: '800', color: '#66520B'},
            {name: '700', color: '#99781B'},
            {name: '600', color: '#CC9B32'},
            {name: '500', color: '#f8bd4f'},
            {name: '400', color: '#FFCA61'},
            {name: '300', color: '#FFD677'},
            {name: '200', color: '#FFE190'},
            {name: '100', color: '#FFEBAD'},
            {name: '050', color: '#FFF4CD'},
            {name: '025', color: '#FFFCF0'},
        ]
        },
        { swatch: 'Grass', colors: [
            {name: '900', color: '#153300'},
            {name: '800', color: '#2C6500'},
            {name: '700', color: '#428D06'},
            {name: '600', color: '#5AAF15'},
            {name: '500', color: '#72cb2a'},
            {name: '400', color: '#87DC42'},
            {name: '300', color: '#9DEA5E'},
            {name: '200', color: '#B3F57D'},
            {name: '100', color: '#C9FCA0'},
            {name: '050', color: '#DFFFC8'},
            {name: '025', color: '#F6FFF0'},
        ]
        },
        { swatch: 'Green', colors: [
            {name: '900', color: '#002E11'},
            {name: '800', color: '#005522'},
            {name: '700', color: '#007633'},
            {name: '600', color: '#009044'},
            {name: '500', color: '#05a455'},
            {name: '400', color: '#28BB70'},
            {name: '300', color: '#50CF8A'},
            {name: '200', color: '#78E0A5'},
            {name: '100', color: '#A0EDC0'},
            {name: '050', color: '#C8F7DA'},
            {name: '025', color: '#F0FDF5'},
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
        gap:1rem;
    }
    div {
        margin-bottom: 4rem;
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


<!-- <section>
    {#each pink as {name, color}}
        <Swatch name={name} color={color} />
    {/each}
</section>
<section>
    {#each purple as {name, color}}
        <Swatch name={name} color={color} />
    {/each}
</section> -->
<script>
    import Swatch from './Swatch.svelte'
    import tinycolor from '../tinycolor'

    function getRatio(swatch){
            let fullRatio = tinycolor.readability(swatch, '#fff');
            let ratio = Math.round((fullRatio + Number.EPSILON) * 100) / 100;
            return ratio;
        }

    let palette = [
        { swatch: 'Red', colors: 
            [
                {name: '900', color: '#290306', ratio: getRatio('#290306')},
                {name: '800', color: '#5E0C12', ratio: getRatio('#5E0C12')},
                {name: '700', color: '#941C24', ratio: getRatio('#941C24')},
                {name: '600', color: '#C0323B', ratio: getRatio('#C0323B')},
                {name: '500', color: '#e44e58', ratio: getRatio('#e44e58')},
                {name: '400', color: '#F3646E', ratio: getRatio('#F3646E')},
                {name: '300', color: '#FD7E87', ratio: getRatio('#FD7E87')},
                {name: '200', color: '#FF9DA4', ratio: getRatio('#FF9DA4')},
                {name: '100', color: '#FFC0C5', ratio: getRatio('#FFC0C5')},
                {name: '050', color: '#FFE7E9', ratio: getRatio('#FFE7E9')},
            ]
            },
        { swatch: 'Orange', colors: 
            [
                {name: '900', color: '#291704', ratio: getRatio('#291704')},
                {name: '800', color: '#5E3710', ratio: getRatio('#5E3710')},
                {name: '700', color: '#945722', ratio: getRatio('#945722')},
                {name: '600', color: '#CA783B', ratio: getRatio('#CA783B')},
                {name: '500', color: '#f69b5a', ratio: getRatio('#f69b5a')},
                {name: '400', color: '#FFAB6E', ratio: getRatio('#FFAB6E')},
                {name: '300', color: '#FFBC85', ratio: getRatio('#FFBC85')},
                {name: '200', color: '#FFCEA2', ratio: getRatio('#FFCEA2')},
                {name: '100', color: '#FFE1C3', ratio: getRatio('#FFE1C3')},
                {name: '050', color: '#FFF4E8', ratio: getRatio('#FFF4E8')},
            ]
            },
        { swatch: 'Yellow', colors: [
            {name: '900', color: '#292202', ratio: getRatio('#292202')},
            {name: '800', color: '#5E4C0B', ratio: getRatio('#5E4C0B')},
            {name: '700', color: '#94741A', ratio: getRatio('#94741A')},
            {name: '600', color: '#CA9931', ratio: getRatio('#CA9931')},
            {name: '500', color: '#f8bd4f', ratio: getRatio('#f8bd4f')},
            {name: '400', color: '#FFCC64', ratio: getRatio('#FFCC64')},
            {name: '300', color: '#FFDA7D', ratio: getRatio('#FFDA7D')},
            {name: '200', color: '#FFE69B', ratio: getRatio('#FFE69B')},
            {name: '100', color: '#FFF1BF', ratio: getRatio('#FFF1BF')},
            {name: '050', color: '#FFFAE7', ratio: getRatio('#FFFAE7')},
        ]
        },
        { swatch: 'Grass', colors: [
            {name: '900', color: '#112900', ratio: getRatio('#112900')},
            {name: '800', color: '#285D00', ratio: getRatio('#285D00')},
            {name: '700', color: '#408806', ratio: getRatio('#408806')},
            {name: '600', color: '#59AD15', ratio: getRatio('#59AD15')},
            {name: '500', color: '#72cb2a', ratio: getRatio('#72cb2a')},
            {name: '400', color: '#8ADF46', ratio: getRatio('#8ADF46')},
            {name: '300', color: '#A3EE66', ratio: getRatio('#A3EE66')},
            {name: '200', color: '#BCF98B', ratio: getRatio('#BCF98B')},
            {name: '100', color: '#D6FFB8', ratio: getRatio('#D6FFB8')},
            {name: '050', color: '#F0FFE6', ratio: getRatio('#F0FFE6')},
        ]
        },
        { swatch: 'Green', colors: [
            {name: '900', color: '#00240E', ratio: getRatio('#00240E')},
            {name: '800', color: '#004E20', ratio: getRatio('#004E20')},
            {name: '700', color: '#007231', ratio: getRatio('#007231')},
            {name: '600', color: '#008E43', ratio: getRatio('#008E43')},
            {name: '500', color: '#05a455', ratio: getRatio('#05a455')},
            {name: '400', color: '#2EBF74', ratio: getRatio('#2EBF74')},
            {name: '300', color: '#5CD592', ratio: getRatio('#5CD592')},
            {name: '200', color: '#8AE7B1', ratio: getRatio('#8AE7B1')},
            {name: '100', color: '#B8F4D0', ratio: getRatio('#B8F4D0')},
            {name: '050', color: '#E6FCEE', ratio: getRatio('#E6FCEE')},
        ]
        },
        { swatch: 'Teal', colors: [
            {name: '900', color: '#0C2728', ratio: getRatio('#0C2728')},
            {name: '800', color: '#1F575A', ratio: getRatio('#1F575A')},
            {name: '700', color: '#378487', ratio: getRatio('#378487')},
            {name: '600', color: '#52ACB0', ratio: getRatio('#52ACB0')},
            {name: '500', color: '#72d1d5', ratio: getRatio('#72d1d5')},
            {name: '400', color: '#85DFE3', ratio: getRatio('#85DFE3')},
            {name: '300', color: '#9BEBEE', ratio: getRatio('#9BEBEE')},
            {name: '200', color: '#B3F4F7', ratio: getRatio('#B3F4F7')},
            {name: '100', color: '#CFFAFC', ratio: getRatio('#CFFAFC')},
            {name: '050', color: '#EDFEFF', ratio: getRatio('#EDFEFF')},
        ]
        },
        { swatch: 'Cyan', colors: [
            {name: '900', color: '#002729', ratio: getRatio('#002729')},
            {name: '800', color: '#07565E', ratio: getRatio('#07565E')},
            {name: '700', color: '#158294', ratio: getRatio('#158294')},
            {name: '600', color: '#2AA9CA', ratio: getRatio('#2AA9CA')},
            {name: '500', color: '#47cdf5', ratio: getRatio('#47cdf5')},
            {name: '400', color: '#5DDCFF', ratio: getRatio('#5DDCFF')},
            {name: '300', color: '#77E9FF', ratio: getRatio('#77E9FF')},
            {name: '200', color: '#97F2FF', ratio: getRatio('#97F2FF')},
            {name: '100', color: '#BCF9FF', ratio: getRatio('#BCF9FF')},
            {name: '050', color: '#E6FEFF', ratio: getRatio('#E6FEFF')},
        ]
        },
        { swatch: 'Blue', colors: [
            {name: '900', color: '#001829', ratio: getRatio('#001829')},
            {name: '800', color: '#06375E', ratio: getRatio('#06375E')},
            {name: '700', color: '#145794', ratio: getRatio('#145794')},
            {name: '600', color: '#2A78CA', ratio: getRatio('#2A78CA')},
            {name: '500', color: '#479aff', ratio: getRatio('#479aff')},
            {name: '400', color: '#5CABFF', ratio: getRatio('#5CABFF')},
            {name: '300', color: '#76BDFF', ratio: getRatio('#76BDFF')},
            {name: '200', color: '#96CFFF', ratio: getRatio('#96CFFF')},
            {name: '100', color: '#BBE1FF', ratio: getRatio('#BBE1FF')},
            {name: '050', color: '#E6F4FF', ratio: getRatio('#E6F4FF')},
        ]
        },
        { swatch: 'Violet', colors: [
            {name: '900', color: '#120C29', ratio: getRatio('#120C29')},
            {name: '800', color: '#2E215E', ratio: getRatio('#2E215E')},
            {name: '700', color: '#4D3C94', ratio: getRatio('#4D3C94')},
            {name: '600', color: '#6F5BCA', ratio: getRatio('#6F5BCA')},
            {name: '500', color: '#9580ff', ratio: getRatio('#9580ff')},
            {name: '400', color: '#A38FFF', ratio: getRatio('#A38FFF')},
            {name: '300', color: '#B3A1FF', ratio: getRatio('#B3A1FF')},
            {name: '200', color: '#C5B7FF', ratio: getRatio('#C5B7FF')},
            {name: '100', color: '#DAD0FF', ratio: getRatio('#DAD0FF')},
            {name: '050', color: '#F1EDFF', ratio: getRatio('#F1EDFF')},
        ]
        },
        { swatch: 'Purple', colors: [
                {name: '900', color: '#1F0C29', ratio: getRatio('#1F0C29')},
                {name: '800', color: '#47215E', ratio: getRatio('#47215E')},
                {name: '700', color: '#6F3C94', ratio: getRatio('#6F3C94')},
                {name: '600', color: '#975BCA', ratio: getRatio('#975BCA')},
                {name: '500', color: '#bf80ff', ratio: getRatio('#bf80ff')},
                {name: '400', color: '#CB8FFF', ratio: getRatio('#CB8FFF')},
                {name: '300', color: '#D6A1FF', ratio: getRatio('#D6A1FF')},
                {name: '200', color: '#E1B7FF', ratio: getRatio('#E1B7FF')},
                {name: '100', color: '#EDD0FF', ratio: getRatio('#EDD0FF')},
                {name: '050', color: '#F9EDFF', ratio: getRatio('#F9EDFF')},
            ]
        },
    { swatch: 'Pink', colors: 
            [
                {name: '900', color: '#290F24', ratio: getRatio('#290F24')},
                {name: '800', color: '#5E2652', ratio: getRatio('#5E2652')},
                {name: '700', color: '#8E417D', ratio: getRatio('#8E417D')},
                {name: '600', color: '#BA60A6', ratio: getRatio('#BA60A6')},
                {name: '500', color: '#e283cd', ratio: getRatio('#e283cd')},
                {name: '400', color: '#EE93DA', ratio: getRatio('#EE93DA')},
                {name: '300', color: '#F6A6E4', ratio: getRatio('#F6A6E4')},
                {name: '200', color: '#FCBCEE', ratio: getRatio('#FCBCEE')},
                {name: '100', color: '#FFD4F6', ratio: getRatio('#FFD4F6')},
                {name: '050', color: '#FFEFFC', ratio: getRatio('#FFEFFC')},
            ]
        },
    { swatch: 'Gray', colors: 
            [
                {name: '900', color: '#1D1D1D', ratio: getRatio('#1D1D1D')},
                {name: '800', color: '#424242', ratio: getRatio('#424242')},
                {name: '700', color: '#686868', ratio: getRatio('#686868')},
                {name: '600', color: '#8D8D8D', ratio: getRatio('#8D8D8D')},
                {name: '500', color: '#b3b3b3', ratio: getRatio('#b3b3b3')},
                {name: '400', color: '#C1C1C1', ratio: getRatio('#C1C1C1')},
                {name: '300', color: '#CECECE', ratio: getRatio('#CECECE')},
                {name: '200', color: '#DCDCDC', ratio: getRatio('#DCDCDC')},
                {name: '100', color: '#EAEAEA', ratio: getRatio('#EAEAEA')},
                {name: '050', color: '#F7F7F7', ratio: getRatio('#F7F7F7')},
            ]
        },
    { swatch: 'Slate', colors: 
            [
                {name: '900', color: '#18191C', ratio: getRatio('#18191C')},
                {name: '800', color: '#393940', ratio: getRatio('#393940')},
                {name: '700', color: '#5A5A64', ratio: getRatio('#5A5A64')},
                {name: '600', color: '#7B7C87', ratio: getRatio('#7B7C87')},
                {name: '500', color: '#9d9eaa', ratio: getRatio('#9d9eaa')},
                {name: '400', color: '#AEAFBA', ratio: getRatio('#AEAFBA')},
                {name: '300', color: '#BFC0CA', ratio: getRatio('#BFC0CA')},
                {name: '200', color: '#D1D1D9', ratio: getRatio('#D1D1D9')},
                {name: '100', color: '#E2E3E8', ratio: getRatio('#E2E3E8')},
                {name: '050', color: '#F5F5F7', ratio: getRatio('#F5F5F7')},
            ]
        },
    { swatch: 'Mist', colors: 
            [
                {name: '900', color: '#191E20', ratio: getRatio('#191E20')},
                {name: '800', color: '#3B4549', ratio: getRatio('#3B4549')},
                {name: '700', color: '#5D6B72', ratio: getRatio('#5D6B72')},
                {name: '600', color: '#819199', ratio: getRatio('#819199')},
                {name: '500', color: '#a6b7bf', ratio: getRatio('#a6b7bf')},
                {name: '400', color: '#B4C5CC', ratio: getRatio('#B4C5CC')},
                {name: '300', color: '#C4D2D9', ratio: getRatio('#C4D2D9')},
                {name: '200', color: '#D3DFE4', ratio: getRatio('#D3DFE4')},
                {name: '100', color: '#E4ECEF', ratio: getRatio('#E4ECEF')},
                {name: '050', color: '#F5F8FA', ratio: getRatio('#F5F8FA')},
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
        flex-wrap: nowrap;
        gap:.5rem;
    }
    div {
        margin-bottom: 1.25rem;
    }
</style>

{#each palette as swatch}
    <div>
        <section>
            {#each swatch.colors.reverse() as {name, color, ratio}}
                <Swatch name="{swatch.swatch}-{name}" {color} {ratio} />
            {/each}
        </section>
    </div>
{/each}
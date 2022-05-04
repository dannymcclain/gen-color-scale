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
                {name: '900', color: '#470000', ratio: getRatio('#470000')},
                {name: '800', color: '#750000', ratio: getRatio('#750000')},
                {name: '700', color: '#A30000', ratio: getRatio('#A30000')},
                {name: '600', color: '#CE000A', ratio: getRatio('#CE000A')},
                {name: '500', color: '#E41120', ratio: getRatio('#E41120')},
                {name: '400', color: '#FA303B', ratio: getRatio('#FA303B')},
                {name: '300', color: '#FF6060', ratio: getRatio('#FF6060')},
                {name: '200', color: '#FF9090', ratio: getRatio('#FF9090')},
                {name: '100', color: '#FFC0C0', ratio: getRatio('#FFC0C0')},
                {name: '050', color: '#FFF0F0', ratio: getRatio('#FFF0F0')},
            ]
            },
        { swatch: 'Red2', colors: 
            [
                {name: '900', color: '#470000', ratio: getRatio('#470000')},
                {name: '800', color: '#750000', ratio: getRatio('#750000')},
                {name: '700', color: '#A30000', ratio: getRatio('#A30000')},
                {name: '600', color: '#CE000A', ratio: getRatio('#CE000A')},
                {name: '500', color: '#E41120', ratio: getRatio('#E41120')},
                {name: '400', color: '#F92D3A', ratio: getRatio('#F92D3A')},
                {name: '300', color: '#FF5A5A', ratio: getRatio('#FF5A5A')},
                {name: '200', color: '#FF8787', ratio: getRatio('#FF8787')},
                {name: '100', color: '#FFB4B4', ratio: getRatio('#FFB4B4')},
                {name: '050', color: '#FFE0E0', ratio: getRatio('#FFE0E0')},
            ]
            },
        { swatch: 'Orange', colors: 
            [
                {name: '900', color: '#471E00', ratio: getRatio('#471E00')},
                {name: '800', color: '#753300', ratio: getRatio('#753300')},
                {name: '700', color: '#A34A00', ratio: getRatio('#A34A00')},
                {name: '600', color: '#D16100', ratio: getRatio('#D16100')},
                {name: '500', color: '#FF7A14', ratio: getRatio('#FF7A14')},
                {name: '400', color: '#FF9130', ratio: getRatio('#FF9130')},
                {name: '300', color: '#FFA860', ratio: getRatio('#FFA860')},
                {name: '200', color: '#FFC190', ratio: getRatio('#FFC190')},
                {name: '100', color: '#FFDBC0', ratio: getRatio('#FFDBC0')},
                {name: '050', color: '#FFF6F0', ratio: getRatio('#FFF6F0')},
            ]
            },
        { swatch: 'Yellow', colors: [
            {name: '900', color: '#473D00', ratio: getRatio('#473D00')},
            {name: '800', color: '#756000', ratio: getRatio('#756000')},
            {name: '700', color: '#A38000', ratio: getRatio('#A38000')},
            {name: '600', color: '#D19E0E', ratio: getRatio('#D19E0E')},
            {name: '500', color: '#FFB829', ratio: getRatio('#FFB829')},
            {name: '400', color: '#FFCA3E', ratio: getRatio('#FFCA3E')},
            {name: '300', color: '#FFDA5B', ratio: getRatio('#FFDA5B')},
            {name: '200', color: '#FFE787', ratio: getRatio('#FFE787')},
            {name: '100', color: '#FFF2B4', ratio: getRatio('#FFF2B4')},
            {name: '050', color: '#FFFBE0', ratio: getRatio('#FFFBE0')},
        ]
        },
        { swatch: 'Grass', colors: [
            {name: '900', color: '#1A4700', ratio: getRatio('#1A4700')},
            {name: '800', color: '#2A6D00', ratio: getRatio('#2A6D00')},
            {name: '700', color: '#3B8B00', ratio: getRatio('#3B8B00')},
            {name: '600', color: '#4DA300', ratio: getRatio('#4DA300')},
            {name: '500', color: '#5EB40E', ratio: getRatio('#5EB40E')},
            {name: '400', color: '#7ACE2D', ratio: getRatio('#7ACE2D')},
            {name: '300', color: '#96E25A', ratio: getRatio('#96E25A')},
            {name: '200', color: '#B2F187', ratio: getRatio('#B2F187')},
            {name: '100', color: '#CFFBB4', ratio: getRatio('#CFFBB4')},
            {name: '050', color: '#EBFFE0', ratio: getRatio('#EBFFE0')},
        ]
        },
        { swatch: 'Green', colors: 
            [
                {name: '900', color: '#003607', ratio: getRatio('#003607')},
                {name: '800', color: '#00520D', ratio: getRatio('#00520D')},
                {name: '700', color: '#006816', ratio: getRatio('#006816')},
                {name: '600', color: '#007920', ratio: getRatio('#007920')},
                {name: '500', color: '#00852C', ratio: getRatio('#00852C')},
                {name: '400', color: '#30A750', ratio: getRatio('#30A750')},
                {name: '300', color: '#60C476', ratio: getRatio('#60C476')},
                {name: '200', color: '#90DB9D', ratio: getRatio('#90DB9D')},
                {name: '100', color: '#C0EEC6', ratio: getRatio('#C0EEC6')},
                {name: '050', color: '#F0FCF1', ratio: getRatio('#F0FCF1')},
            ]
            },
        { swatch: 'Teal', colors: [
            {name: '900', color: '#004747', ratio: getRatio('#004747')},
            {name: '800', color: '#007575', ratio: getRatio('#007575')},
            {name: '700', color: '#009CA2', ratio: getRatio('#009CA2')},
            {name: '600', color: '#0AB8BF', ratio: getRatio('#0AB8BF')},
            {name: '500', color: '#20CED5', ratio: getRatio('#20CED5')},
            {name: '400', color: '#3AE3EA', ratio: getRatio('#3AE3EA')},
            {name: '300', color: '#5AF3F9', ratio: getRatio('#5AF3F9')},
            {name: '200', color: '#87FEFF', ratio: getRatio('#87FEFF')},
            {name: '100', color: '#B4FFFF', ratio: getRatio('#B4FFFF')},
            {name: '050', color: '#E0FFFF', ratio: getRatio('#E0FFFF')},
        ]
        },
        { swatch: 'Cyan', colors: [
            {name: '900', color: '#00353D', ratio: getRatio('#00353D')},
            {name: '800', color: '#005B6E', ratio: getRatio('#005B6E')},
            {name: '700', color: '#007E9E', ratio: getRatio('#007E9E')},
            {name: '600', color: '#0D9DCF', ratio: getRatio('#0D9DCF')},
            {name: '500', color: '#28b8f6', ratio: getRatio('#28b8f6')},
            {name: '400', color: '#3FCCFF', ratio: getRatio('#3FCCFF')},
            {name: '300', color: '#5EDCFF', ratio: getRatio('#5EDCFF')},
            {name: '200', color: '#8DEAFF', ratio: getRatio('#8DEAFF')},
            {name: '100', color: '#BCF5FF', ratio: getRatio('#BCF5FF')},
            {name: '050', color: '#EBFDFF', ratio: getRatio('#EBFDFF')},
        ]
        },
        { swatch: 'Blue', colors: 

            [
                {name: '900', color: '#001C47', ratio: getRatio('#001C47')},
                {name: '800', color: '#003075', ratio: getRatio('#003075')},
                {name: '700', color: '#0044A3', ratio: getRatio('#0044A3')},
                {name: '600', color: '#0158C4', ratio: getRatio('#0158C4')},
                {name: '500', color: '#176ed9', ratio: getRatio('#176ed9')},
                {name: '400', color: '#3388F0', ratio: getRatio('#3388F0')},
                {name: '300', color: '#60A2FF', ratio: getRatio('#60A2FF')},
                {name: '200', color: '#90BDFF', ratio: getRatio('#90BDFF')},
                {name: '100', color: '#C0D9FF', ratio: getRatio('#C0D9FF')},
                {name: '050', color: '#F0F6FF', ratio: getRatio('#F0F6FF')},
            ]
            },
        { swatch: 'Violet', colors: [
            {name: '900', color: '#170D3D', ratio: getRatio('#170D3D')},
            {name: '800', color: '#2F1E6E', ratio: getRatio('#2F1E6E')},
            {name: '700', color: '#4A359E', ratio: getRatio('#4A359E')},
            {name: '600', color: '#6952CF', ratio: getRatio('#6952CF')},
            {name: '500', color: '#8c75ff', ratio: getRatio('#8c75ff')},
            {name: '400', color: '#9A84FF', ratio: getRatio('#9A84FF')},
            {name: '300', color: '#AB97FF', ratio: getRatio('#AB97FF')},
            {name: '200', color: '#C0AFFF', ratio: getRatio('#C0AFFF')},
            {name: '100', color: '#D7CDFF', ratio: getRatio('#D7CDFF')},
            {name: '050', color: '#F2EFFF', ratio: getRatio('#F2EFFF')},
        ]
        },
        { swatch: 'Purple', colors: [
                {name: '900', color: '#2D0D3D', ratio: getRatio('#2D0D3D')},
                {name: '800', color: '#501E6E', ratio: getRatio('#501E6E')},
                {name: '700', color: '#73359E', ratio: getRatio('#73359E')},
                {name: '600', color: '#9752CF', ratio: getRatio('#9752CF')},
                {name: '500', color: '#ba75ff', ratio: getRatio('#ba75ff')},
                {name: '400', color: '#C784FF', ratio: getRatio('#C784FF')},
                {name: '300', color: '#D397FF', ratio: getRatio('#D397FF')},
                {name: '200', color: '#E0AFFF', ratio: getRatio('#E0AFFF')},
                {name: '100', color: '#EDCDFF', ratio: getRatio('#EDCDFF')},
                {name: '050', color: '#FAEFFF', ratio: getRatio('#FAEFFF')},
            ]
        },
    { swatch: 'Pink', colors: 
            [
                {name: '900', color: '#3D0C3A', ratio: getRatio('#3D0C3A')},
                {name: '800', color: '#6E1D64', ratio: getRatio('#6E1D64')},
                {name: '700', color: '#9E328C', ratio: getRatio('#9E328C')},
                {name: '600', color: '#CC4DB0', ratio: getRatio('#CC4DB0')},
                {name: '500', color: '#ed6ed1', ratio: getRatio('#ed6ed1')},
                {name: '400', color: '#FA7FDF', ratio: getRatio('#FA7FDF')},
                {name: '300', color: '#FF94EB', ratio: getRatio('#FF94EB')},
                {name: '200', color: '#FFAEF4', ratio: getRatio('#FFAEF4')},
                {name: '100', color: '#FFCCFA', ratio: getRatio('#FFCCFA')},
                {name: '050', color: '#FFEFFE', ratio: getRatio('#FFEFFE')},
            ]
        },
    { swatch: 'Gray', colors: 
            [
                {name: '900', color: '#282828', ratio: getRatio('#282828')},
                {name: '800', color: '#484848', ratio: getRatio('#484848')},
                {name: '700', color: '#686868', ratio: getRatio('#686868')},
                {name: '600', color: '#888888', ratio: getRatio('#888888')},
                {name: '500', color: '#a8a8a8', ratio: getRatio('#a8a8a8')},
                {name: '400', color: '#B8B8B8', ratio: getRatio('#B8B8B8')},
                {name: '300', color: '#C8C8C8', ratio: getRatio('#C8C8C8')},
                {name: '200', color: '#D8D8D8', ratio: getRatio('#D8D8D8')},
                {name: '100', color: '#E8E8E8', ratio: getRatio('#E8E8E8')},
                {name: '050', color: '#F8F8F8', ratio: getRatio('#F8F8F8')},
            ]
        },
    { swatch: 'Slate', colors: 
            [
                {name: '900', color: '#22232A', ratio: getRatio('#22232A')},
                {name: '800', color: '#3E404A', ratio: getRatio('#3E404A')},
                {name: '700', color: '#5B5D69', ratio: getRatio('#5B5D69')},
                {name: '600', color: '#787A88', ratio: getRatio('#787A88')},
                {name: '500', color: '#9698a6', ratio: getRatio('#9698a6')},
                {name: '400', color: '#A8AAB8', ratio: getRatio('#A8AAB8')},
                {name: '300', color: '#BBBCC9', ratio: getRatio('#BBBCC9')},
                {name: '200', color: '#CECFD9', ratio: getRatio('#CECFD9')},
                {name: '100', color: '#E2E3E9', ratio: getRatio('#E2E3E9')},
                {name: '050', color: '#F6F6F9', ratio: getRatio('#F6F6F9')},
            ]
        },
    { swatch: 'Mist', colors: 
            [
                {name: '900', color: '#212B30', ratio: getRatio('#212B30')},
                {name: '800', color: '#3D4D54', ratio: getRatio('#3D4D54')},
                {name: '700', color: '#5A6D77', ratio: getRatio('#5A6D77')},
                {name: '600', color: '#798E98', ratio: getRatio('#798E98')},
                {name: '500', color: '#99aeb8', ratio: getRatio('#99aeb8')},
                {name: '400', color: '#A9BEC8', ratio: getRatio('#A9BEC8')},
                {name: '300', color: '#BBCDD6', ratio: getRatio('#BBCDD6')},
                {name: '200', color: '#CDDCE3', ratio: getRatio('#CDDCE3')},
                {name: '100', color: '#E1EBEF', ratio: getRatio('#E1EBEF')},
                {name: '050', color: '#F6F9FB', ratio: getRatio('#F6F9FB')},
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
        // gap:.5rem;
        gap:0;
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
{#each palette as swatch}
    <h3>{swatch.swatch}</h3>
    <ul>
        {#each swatch.colors as {name, color}}
            <li>{swatch.swatch.toLowerCase()}-{name}: {color}</li>
        {/each}
    </ul>
{/each}
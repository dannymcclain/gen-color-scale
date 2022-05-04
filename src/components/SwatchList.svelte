<script>
    import Swatch from './Swatch.svelte'
    import tinycolor from '../tinycolor'

    function getRatio(swatch){
            let fullRatio = tinycolor.readability(swatch, '#fff');
            let ratio = Math.round((fullRatio + Number.EPSILON) * 100) / 100;
            return ratio;
        }

    let palette = [
        { swatch: 'Blue 2', colors: 

            [
                {name: '900', color: '#001C47', ratio: getRatio('#001C47')},
                {name: '800', color: '#003075', ratio: getRatio('#003075')},
                {name: '700', color: '#0044A3', ratio: getRatio('#0044A3')},
                {name: '600', color: '#0158C4', ratio: getRatio('#0158C4')},
                {name: '500-Base', color: '#176ed9', ratio: getRatio('#176ed9')},
                {name: '400', color: '#3388F0', ratio: getRatio('#3388F0')},
                {name: '300', color: '#60A2FF', ratio: getRatio('#60A2FF')},
                {name: '200', color: '#90BDFF', ratio: getRatio('#90BDFF')},
                {name: '100', color: '#C0D9FF', ratio: getRatio('#C0D9FF')},
                {name: '050', color: '#F0F6FF', ratio: getRatio('#F0F6FF')},
            ]
            },
        { swatch: 'Green 2', colors: 
            [
                {name: '900', color: '#003613', ratio: getRatio('#003613')},
                {name: '800', color: '#00511F', ratio: getRatio('#00511F')},
                {name: '700', color: '#00672B', ratio: getRatio('#00672B')},
                {name: '600', color: '#007837', ratio: getRatio('#007837')},
                {name: '500-Base', color: '#018443', ratio: getRatio('#018443')},
                {name: '400', color: '#30A666', ratio: getRatio('#30A666')},
                {name: '300', color: '#60C38A', ratio: getRatio('#60C38A')},
                {name: '200', color: '#90DBAD', ratio: getRatio('#90DBAD')},
                {name: '100', color: '#C0EED1', ratio: getRatio('#C0EED1')},
                {name: '050', color: '#F0FCF4', ratio: getRatio('#F0FCF4')},
            ]
            },
        { swatch: 'Green 3', colors: 
            [
                {name: '900', color: '#003607', ratio: getRatio('#003607')},
                {name: '800', color: '#00520D', ratio: getRatio('#00520D')},
                {name: '700', color: '#006816', ratio: getRatio('#006816')},
                {name: '600', color: '#007920', ratio: getRatio('#007920')},
                {name: '500-Base', color: '#00852C', ratio: getRatio('#00852C')},
                {name: '400', color: '#30A750', ratio: getRatio('#30A750')},
                {name: '300', color: '#60C476', ratio: getRatio('#60C476')},
                {name: '200', color: '#90DB9D', ratio: getRatio('#90DB9D')},
                {name: '100', color: '#C0EEC6', ratio: getRatio('#C0EEC6')},
                {name: '050', color: '#F0FCF1', ratio: getRatio('#F0FCF1')},
            ]
            },
        { swatch: 'Red 3', colors: 
            [
                {name: '900', color: '#470000', ratio: getRatio('#470000')},
                {name: '800', color: '#750000', ratio: getRatio('#750000')},
                {name: '700', color: '#A30000', ratio: getRatio('#A30000')},
                {name: '600', color: '#CE000A', ratio: getRatio('#CE000A')},
                {name: '500-Base', color: '#E41120', ratio: getRatio('#E41120')},
                {name: '400', color: '#FA303B', ratio: getRatio('#FA303B')},
                {name: '300', color: '#FF6060', ratio: getRatio('#FF6060')},
                {name: '200', color: '#FF9090', ratio: getRatio('#FF9090')},
                {name: '100', color: '#FFC0C0', ratio: getRatio('#FFC0C0')},
                {name: '050', color: '#FFF0F0', ratio: getRatio('#FFF0F0')},
            ]
            },
        { swatch: 'Red 2', colors: 
            [
                {name: '900', color: '#470002', ratio: getRatio('#470002')},
                {name: '800', color: '#75020B', ratio: getRatio('#75020B')},
                {name: '700', color: '#A30F1A', ratio: getRatio('#A30F1A')},
                {name: '600', color: '#D0232F', ratio: getRatio('#D0232F')},
                {name: '500-Base', color: '#ea3e4a', ratio: getRatio('#ea3e4a')},
                {name: '400', color: '#FC5460', ratio: getRatio('#FC5460')},
                {name: '300', color: '#FF717C', ratio: getRatio('#FF717C')},
                {name: '200', color: '#FF949D', ratio: getRatio('#FF949D')},
                {name: '100', color: '#FFC0C3', ratio: getRatio('#FFC0C3')},
                {name: '050', color: '#FFF0F0', ratio: getRatio('#FFF0F0')},
            ]
            },
        { swatch: 'Red', colors: 
            [
                {name: '900', color: '#3D0004', ratio: getRatio('#3D0004')},
                {name: '800', color: '#6E060E', ratio: getRatio('#6E060E')},
                {name: '700', color: '#9E141E', ratio: getRatio('#9E141E')},
                {name: '600', color: '#CA2A35', ratio: getRatio('#CA2A35')},
                {name: '500', color: '#e74651', ratio: getRatio('#e74651')},
                {name: '400', color: '#F85B66', ratio: getRatio('#F85B66')},
                {name: '300', color: '#FF7780', ratio: getRatio('#FF7780')},
                {name: '200', color: '#FF979F', ratio: getRatio('#FF979F')},
                {name: '100', color: '#FFBEC3', ratio: getRatio('#FFBEC3')},
                {name: '050', color: '#FFEBEC', ratio: getRatio('#FFEBEC')},
            ]
            },
        { swatch: 'Orange', colors: 
            [
                {name: '900', color: '#3D2000', ratio: getRatio('#3D2000')},
                {name: '800', color: '#6E3B04', ratio: getRatio('#6E3B04')},
                {name: '700', color: '#9E5613', ratio: getRatio('#9E5613')},
                {name: '600', color: '#CF7429', ratio: getRatio('#CF7429')},
                {name: '500', color: '#fa9247', ratio: getRatio('#fa9247')},
                {name: '400', color: '#FFA45B', ratio: getRatio('#FFA45B')},
                {name: '300', color: '#FFB775', ratio: getRatio('#FFB775')},
                {name: '200', color: '#FFCA96', ratio: getRatio('#FFCA96')},
                {name: '100', color: '#FFDFBC', ratio: getRatio('#FFDFBC')},
                {name: '050', color: '#FFF5EB', ratio: getRatio('#FFF5EB')},
            ]
            },
        { swatch: 'Yellow', colors: [
            {name: '900', color: '#3D3200', ratio: getRatio('#3D3200')},
            {name: '800', color: '#6E5802', ratio: getRatio('#6E5802')},
            {name: '700', color: '#9E7A10', ratio: getRatio('#9E7A10')},
            {name: '600', color: '#CF9B25', ratio: getRatio('#CF9B25')},
            {name: '500', color: '#f9b943', ratio: getRatio('#f9b943')},
            {name: '400', color: '#FFCA57', ratio: getRatio('#FFCA57')},
            {name: '300', color: '#FFD972', ratio: getRatio('#FFD972')},
            {name: '200', color: '#FFE793', ratio: getRatio('#FFE793')},
            {name: '100', color: '#FFF2BC', ratio: getRatio('#FFF2BC')},
            {name: '050', color: '#FFFCEB', ratio: getRatio('#FFFCEB')},
        ]
        },
        { swatch: 'Grass', colors: [
            {name: '900', color: '#183D00', ratio: getRatio('#183D00')},
            {name: '800', color: '#2D6E00', ratio: getRatio('#2D6E00')},
            {name: '700', color: '#419300', ratio: getRatio('#419300')},
            {name: '600', color: '#57B10D', ratio: getRatio('#57B10D')},
            {name: '500', color: '#6dc723', ratio: getRatio('#6dc723')},
            {name: '400', color: '#87DE3F', ratio: getRatio('#87DE3F')},
            {name: '300', color: '#A1F060', ratio: getRatio('#A1F060')},
            {name: '200', color: '#BCFB8D', ratio: getRatio('#BCFB8D')},
            {name: '100', color: '#D7FFBC', ratio: getRatio('#D7FFBC')},
            {name: '050', color: '#F3FFEB', ratio: getRatio('#F3FFEB')},
        ]
        },
        { swatch: 'Green', colors: [
            {name: '900', color: '#003814', ratio: getRatio('#003814')},
            {name: '800', color: '#005C23', ratio: getRatio('#005C23')},
            {name: '700', color: '#007A33', ratio: getRatio('#007A33')},
            {name: '600', color: '#009043', ratio: getRatio('#009043')},
            {name: '500', color: '#03a052', ratio: getRatio('#03a052')},
            {name: '400', color: '#2FBE72', ratio: getRatio('#2FBE72')},
            {name: '300', color: '#5ED692', ratio: getRatio('#5ED692')},
            {name: '200', color: '#8DE9B2', ratio: getRatio('#8DE9B2')},
            {name: '100', color: '#BCF6D1', ratio: getRatio('#BCF6D1')},
            {name: '050', color: '#EBFDF1', ratio: getRatio('#EBFDF1')},
        ]
        },
        { swatch: 'Teal', colors: [
            {name: '900', color: '#003D3D', ratio: getRatio('#003D3D')},
            {name: '800', color: '#016E6E', ratio: getRatio('#016E6E')},
            {name: '700', color: '#0C9C9E', ratio: getRatio('#0C9C9E')},
            {name: '600', color: '#20BDC4', ratio: getRatio('#20BDC4')},
            {name: '500', color: '#3ad8df', ratio: getRatio('#3ad8df')},
            {name: '400', color: '#51EBF2', ratio: getRatio('#51EBF2')},
            {name: '300', color: '#6FF9FF', ratio: getRatio('#6FF9FF')},
            {name: '200', color: '#92FFFF', ratio: getRatio('#92FFFF')},
            {name: '100', color: '#BCFFFF', ratio: getRatio('#BCFFFF')},
            {name: '050', color: '#EBFFFF', ratio: getRatio('#EBFFFF')},
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
        { swatch: 'Deep Blue', colors: [
            {name: '900', color: '#00183D', ratio: getRatio('#00183D')},
            {name: '800', color: '#002C6E', ratio: getRatio('#002C6E')},
            {name: '700', color: '#00419E', ratio: getRatio('#00419E')},
            {name: '600', color: '#0157C2', ratio: getRatio('#0157C2')},
            {name: '500', color: '#176ed9', ratio: getRatio('#176ed9')},
            {name: '400', color: '#3387EF', ratio: getRatio('#3387EF')},
            {name: '300', color: '#5EA1FF', ratio: getRatio('#5EA1FF')},
            {name: '200', color: '#8DBCFF', ratio: getRatio('#8DBCFF')},
            {name: '100', color: '#BCD7FF', ratio: getRatio('#BCD7FF')},
            {name: '050', color: '#EBF3FF', ratio: getRatio('#EBF3FF')},
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
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
                {name: 'red', color: '#db351f', get ratio() { return getRatio(this.color)}},
                {name: 'navy-muted', color: '#272f46', get ratio() { return getRatio(this.color)}},
                {name: 'navy', color: '#0c1733', get ratio() { return getRatio(this.color)}},
                {name: 'white', color: '#ffffff', get ratio() { return getRatio(this.color)}},
                
            ]
        },
        { swatch: 'rose', colors:
            [
                {name: '900', color: '#470000', get ratio() { return getRatio(this.color)}},
                {name: '800', color: '#750007', get ratio() { return getRatio(this.color)}},
                {name: '700', color: '#A30814', get ratio() { return getRatio(this.color)}},
                {name: '600', color: '#D01B28', get ratio() { return getRatio(this.color)}},
                {name: '500', color: '#e93542', get ratio() { return getRatio(this.color)}},
                {name: '400', color: '#FB4C58', get ratio() { return getRatio(this.color)}},
                {name: '300', color: '#FF6874', get ratio() { return getRatio(this.color)}},
                {name: '200', color: '#FF8B94', get ratio() { return getRatio(this.color)}},
                {name: '100', color: '#FFB8BA', get ratio() { return getRatio(this.color)}},
                {name: '050', color: '#FFE6E6', get ratio() { return getRatio(this.color)}},
            ]
        },
        { swatch: 'orange', colors:
            [
                {name: '900', color: '#472200', get ratio() { return getRatio(this.color)}},
                {name: '800', color: '#753900', get ratio() { return getRatio(this.color)}},
                {name: '700', color: '#A35200', get ratio() { return getRatio(this.color)}},
                {name: '600', color: '#D16B12', get ratio() { return getRatio(this.color)}},
                {name: '500', color: '#fb862d', get ratio() { return getRatio(this.color)}},
                {name: '400', color: '#FF9A43', get ratio() { return getRatio(this.color)}},
                {name: '300', color: '#FFAE60', get ratio() { return getRatio(this.color)}},
                {name: '200', color: '#FFC48A', get ratio() { return getRatio(this.color)}},
                {name: '100', color: '#FFDAB8', get ratio() { return getRatio(this.color)}},
                {name: '050', color: '#FFF2E6', get ratio() { return getRatio(this.color)}},
            ]
        },
        { swatch: 'yellow', colors:
            [
                {name: '900', color: '#473D00', get ratio() { return getRatio(this.color)}},
                {name: '800', color: '#756000', get ratio() { return getRatio(this.color)}},
                {name: '700', color: '#A38000', get ratio() { return getRatio(this.color)}},
                {name: '600', color: '#D19E0E', get ratio() { return getRatio(this.color)}},
                {name: '500', color: '#ffb829', get ratio() { return getRatio(this.color)}},
                {name: '400', color: '#FFCA3F', get ratio() { return getRatio(this.color)}},
                {name: '300', color: '#FFDA5C', get ratio() { return getRatio(this.color)}},
                {name: '200', color: '#FFE88A', get ratio() { return getRatio(this.color)}},
                {name: '100', color: '#FFF3B8', get ratio() { return getRatio(this.color)}},
                {name: '050', color: '#FFFBE6', get ratio() { return getRatio(this.color)}},
            ]
        },
        { swatch: 'grass', colors:
            [
                {name: '900', color: '#1A4700', get ratio() { return getRatio(this.color)}},
                {name: '800', color: '#2A6D00', get ratio() { return getRatio(this.color)}},
                {name: '700', color: '#3B8B00', get ratio() { return getRatio(this.color)}},
                {name: '600', color: '#4DA300', get ratio() { return getRatio(this.color)}},
                {name: '500', color: '#5eb40e', get ratio() { return getRatio(this.color)}},
                {name: '400', color: '#7BCE2E', get ratio() { return getRatio(this.color)}},
                {name: '300', color: '#97E35C', get ratio() { return getRatio(this.color)}},
                {name: '200', color: '#B4F28A', get ratio() { return getRatio(this.color)}},
                {name: '100', color: '#D1FCB8', get ratio() { return getRatio(this.color)}},
                {name: '050', color: '#EFFFE6', get ratio() { return getRatio(this.color)}},
            ]
        },
        { swatch: 'green', colors:
            [
                {name: '900', color: '#003F09', get ratio() { return getRatio(this.color)}},
                {name: '800', color: '#005F11', get ratio() { return getRatio(this.color)}},
                {name: '700', color: '#00791B', get ratio() { return getRatio(this.color)}},
                {name: '600', color: '#008D28', get ratio() { return getRatio(this.color)}},
                {name: '500', color: '#039b36', get ratio() { return getRatio(this.color)}},
                {name: '400', color: '#2EB956', get ratio() { return getRatio(this.color)}},
                {name: '300', color: '#5CD178', get ratio() { return getRatio(this.color)}},
                {name: '200', color: '#8AE59C', get ratio() { return getRatio(this.color)}},
                {name: '100', color: '#B8F3C2', get ratio() { return getRatio(this.color)}},
                {name: '050', color: '#E6FCE9', get ratio() { return getRatio(this.color)}},
            ]
        },
        { swatch: 'teal', colors:
            [
                {name: '900', color: '#004747', get ratio() { return getRatio(this.color)}},
                {name: '800', color: '#007575', get ratio() { return getRatio(this.color)}},
                {name: '700', color: '#009CA2', get ratio() { return getRatio(this.color)}},
                {name: '600', color: '#0AB8BF', get ratio() { return getRatio(this.color)}},
                {name: '500', color: '#20CED5', get ratio() { return getRatio(this.color)}},
                {name: '400', color: '#42DCE3', get ratio() { return getRatio(this.color)}},
                {name: '300', color: '#67E8ED', get ratio() { return getRatio(this.color)}},
                {name: '200', color: '#8EF2F6', get ratio() { return getRatio(this.color)}},
                {name: '100', color: '#B9F9FB', get ratio() { return getRatio(this.color)}},
                {name: '050', color: '#E6FDFE', get ratio() { return getRatio(this.color)}},
            ]
        },
        { swatch: 'sky', colors:
            [
                {name: '900', color: '#003E47', get ratio() { return getRatio(this.color)}},
                {name: '800', color: '#006075', get ratio() { return getRatio(this.color)}},
                {name: '700', color: '#007FA3', get ratio() { return getRatio(this.color)}},
                {name: '600', color: '#0099D1', get ratio() { return getRatio(this.color)}},
                {name: '500', color: '#05b0fa', get ratio() { return getRatio(this.color)}},
                {name: '400', color: '#2EC6FF', get ratio() { return getRatio(this.color)}},
                {name: '300', color: '#5CD8FF', get ratio() { return getRatio(this.color)}},
                {name: '200', color: '#8AE7FF', get ratio() { return getRatio(this.color)}},
                {name: '100', color: '#B8F3FF', get ratio() { return getRatio(this.color)}},
                {name: '050', color: '#E6FCFF', get ratio() { return getRatio(this.color)}},
            ]
        },
        { swatch: 'blue', colors:
            [
                {name: '900', color: '#002247', get ratio() { return getRatio(this.color)}},
                {name: '800', color: '#003975', get ratio() { return getRatio(this.color)}},
                {name: '700', color: '#0150A3', get ratio() { return getRatio(this.color)}},
                {name: '600', color: '#1369D1', get ratio() { return getRatio(this.color)}},
                {name: '500', color: '#2d82eb', get ratio() { return getRatio(this.color)}},
                {name: '400', color: '#4497FD', get ratio() { return getRatio(this.color)}},
                {name: '300', color: '#62ADFF', get ratio() { return getRatio(this.color)}},
                {name: '200', color: '#8AC3FF', get ratio() { return getRatio(this.color)}},
                {name: '100', color: '#B8DAFF', get ratio() { return getRatio(this.color)}},
                {name: '050', color: '#E6F2FF', get ratio() { return getRatio(this.color)}},
            ]
        },
        { swatch: 'violet', colors:
            [
                {name: '900', color: '#1E1347', get ratio() { return getRatio(this.color)}},
                {name: '800', color: '#352675', get ratio() { return getRatio(this.color)}},
                {name: '700', color: '#503DA3', get ratio() { return getRatio(this.color)}},
                {name: '600', color: '#6E5AD1', get ratio() { return getRatio(this.color)}},
                {name: '500', color: '#8f7bf4', get ratio() { return getRatio(this.color)}},
                {name: '400', color: '#9D89FF', get ratio() { return getRatio(this.color)}},
                {name: '300', color: '#AE9CFF', get ratio() { return getRatio(this.color)}},
                {name: '200', color: '#C1B3FF', get ratio() { return getRatio(this.color)}},
                {name: '100', color: '#D7CDFF', get ratio() { return getRatio(this.color)}},
                {name: '050', color: '#F0ECFF', get ratio() { return getRatio(this.color)}},
            ]
        },
        { swatch: 'purple', colors:
            [
                {name: '900', color: '#320E47', get ratio() { return getRatio(this.color)}},
                {name: '800', color: '#531D75', get ratio() { return getRatio(this.color)}},
                {name: '700', color: '#7333A3', get ratio() { return getRatio(this.color)}},
                {name: '600', color: '#934ED1', get ratio() { return getRatio(this.color)}},
                {name: '500', color: '#b36ef7', get ratio() { return getRatio(this.color)}},
                {name: '400', color: '#C17EFF', get ratio() { return getRatio(this.color)}},
                {name: '300', color: '#CF92FF', get ratio() { return getRatio(this.color)}},
                {name: '200', color: '#DCABFF', get ratio() { return getRatio(this.color)}},
                {name: '100', color: '#EAC8FF', get ratio() { return getRatio(this.color)}},
                {name: '050', color: '#F7EAFF', get ratio() { return getRatio(this.color)}},
            ]
        },
        { swatch: 'pink', colors:
            [
                {name: '900', color: '#470E44', get ratio() { return getRatio(this.color)}},
                {name: '800', color: '#751D6C', get ratio() { return getRatio(this.color)}},
                {name: '700', color: '#A33291', get ratio() { return getRatio(this.color)}},
                {name: '600', color: '#D04DB3', get ratio() { return getRatio(this.color)}},
                {name: '500', color: '#ef6cd2', get ratio() { return getRatio(this.color)}},
                {name: '400', color: '#FC7CE0', get ratio() { return getRatio(this.color)}},
                {name: '300', color: '#FF91EB', get ratio() { return getRatio(this.color)}},
                {name: '200', color: '#FFAAF4', get ratio() { return getRatio(this.color)}},
                {name: '100', color: '#FFC8FA', get ratio() { return getRatio(this.color)}},
                {name: '050', color: '#FFEAFE', get ratio() { return getRatio(this.color)}},
            ]
        },
        { swatch: 'gray', colors:
            [
                {name: '900', color: '#2F2F2F', get ratio() { return getRatio(this.color)}},
                {name: '800', color: '#4D4D4D', get ratio() { return getRatio(this.color)}},
                {name: '700', color: '#6C6C6C', get ratio() { return getRatio(this.color)}},
                {name: '600', color: '#8A8A8A', get ratio() { return getRatio(this.color)}},
                {name: '500', color: '#a8a8a8', get ratio() { return getRatio(this.color)}},
                {name: '400', color: '#B8B8B8', get ratio() { return getRatio(this.color)}},
                {name: '300', color: '#C7C7C7', get ratio() { return getRatio(this.color)}},
                {name: '200', color: '#D7D7D7', get ratio() { return getRatio(this.color)}},
                {name: '100', color: '#E7E7E7', get ratio() { return getRatio(this.color)}},
                {name: '050', color: '#F6F6F6', get ratio() { return getRatio(this.color)}},
            ]
        },
        { swatch: 'slate', colors:
            [
                {name: '900', color: '#282931', get ratio() { return getRatio(this.color)}},
                {name: '800', color: '#43444F', get ratio() { return getRatio(this.color)}},
                {name: '700', color: '#5E606D', get ratio() { return getRatio(this.color)}},
                {name: '600', color: '#7A7C8A', get ratio() { return getRatio(this.color)}},
                {name: '500', color: '#9698a6', get ratio() { return getRatio(this.color)}},
                {name: '400', color: '#A8AAB7', get ratio() { return getRatio(this.color)}},
                {name: '300', color: '#BABCC8', get ratio() { return getRatio(this.color)}},
                {name: '200', color: '#CDCED8', get ratio() { return getRatio(this.color)}},
                {name: '100', color: '#E0E1E8', get ratio() { return getRatio(this.color)}},
                {name: '050', color: '#F4F4F7', get ratio() { return getRatio(this.color)}},
            ]
        },
        { swatch: 'mist', colors:
            [
                {name: '900', color: '#273237', get ratio() { return getRatio(this.color)}},
                {name: '800', color: '#42525A', get ratio() { return getRatio(this.color)}},
                {name: '700', color: '#5E717A', get ratio() { return getRatio(this.color)}},
                {name: '600', color: '#7B909A', get ratio() { return getRatio(this.color)}},
                {name: '500', color: '#99aeb8', get ratio() { return getRatio(this.color)}},
                {name: '400', color: '#A9BDC7', get ratio() { return getRatio(this.color)}},
                {name: '300', color: '#BACDD5', get ratio() { return getRatio(this.color)}},
                {name: '200', color: '#CCDBE2', get ratio() { return getRatio(this.color)}},
                {name: '100', color: '#DFEAEE', get ratio() { return getRatio(this.color)}},
                {name: '050', color: '#F3F7F9', get ratio() { return getRatio(this.color)}},
            ]
        },
    ];
    
    let functionalFoundations = [
        {
            "swatch": "foreground",
            "colors": [
                {
                    "name": "fg/fg-default",
                    "color": "#0c1733",
                    "description": "built-navy, 17.71"
                },
                {
                    "name": "fg/fg-muted",
                    "color": "#43444F",
                    "description": "slate-800, 9.64"
                },
                {
                    "name": "fg/fg-muted",
                    "color": "#43444F",
                    "description": "slate-800, 9.64"
                },
                {
                    "name": "fg/fg-disabled",
                    "color": "#9698a6",
                    "description": "slate-500, 2.86"
                },
                {
                    "name": "fg/fg-roleEmphasis",
                    "color": "#FFFFFF",
                    "description": "built-white, 1"
                }
            ]
        },
        {
            "swatch": "background",
            "colors": [
                {
                    "name": "bg/bg-default",
                    "color": "#FFFFFF",
                    "description": "built-white, 1"
                },
                {
                    "name": "bg/bg-subtle",
                    "color": "#f3f7f9",
                    "description": "mist-50, 1.08"
                },
                {
                    "name": "bg/bg-heavy",
                    "color": "#dfeaee",
                    "description": "mist-100, 1.23"
                }
            ]
        },
        {
            "swatch": "divider",
            "colors": [
                {
                    "name": "divider/divider-faint",
                    "color": "#F4F4F7",
                    "description": "slate-50, 1.1"
                },
                {
                    "name": "divider/divider-light",
                    "color": "#E0E1E8",
                    "description": "slate-100, 1.3"
                },
                {
                    "name": "divider/divider-default",
                    "color": "#CDCED8",
                    "description": "slate-200, 1.57"
                },
                {
                    "name": "divider/divider-heavy",
                    "color": "#A8AAB7",
                    "description": "slate-400, 2.31"
                }
            ]
        }
    ];
    let stringFunctionalFoundations = JSON.stringify(functionalFoundations, null, 4);
    let stringColorScale;
    function formatPalette() {
        let formattedPalette = JSON.parse(JSON.stringify(colorPalette));
        formattedPalette.forEach(item => {
            let name = item.swatch;
            let colors = item.colors.reverse();
            colors.forEach(color => {
                if (color.name === '050'){
                    color.name = '50';
                }
                color.name = name + '-' + color.name;
                color['description'] = color['ratio'];
                color.description = color.color + ', ' + color.ratio.toString();
            })
        });
        stringColorScale = JSON.stringify(formattedPalette, null, 4);
    }
    formatPalette();

    // function justAnIdea() {
    //     let someSwatch = JSON.parse(JSON.stringify(colorPalette[0].colors[0]));
    //     someSwatch.readability = tinycolor.isReadable(someSwatch.color, "#fff");
    //     console.log(someSwatch);
    // }
    // justAnIdea();

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
            {#each swatch.colors.reverse() as {name, color, ratio}}
                <Swatch name="{swatch.swatch}-{name}" {color} {ratio} />
            {/each}
        </section>
    </div>
{/each}

<section class="object">
    <h2>Color Scale</h2>
    <!-- <p>A reformatted object of the color scale to use with the Figma plugin I made.</p> -->
    <button on:click={() => updateClipboard(stringColorScale)}>Copy</button>
    <pre>{stringColorScale}</pre>
</section>
<section class="object">
    <h2>Functional Foundations</h2>
    <button on:click={() => updateClipboard(stringFunctionalFoundations)}>Copy</button>
    <pre>{stringFunctionalFoundations}</pre>
</section>
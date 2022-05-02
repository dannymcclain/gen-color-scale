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
                {name: '400', color: '#F36E77'},
                {name: '300', color: '#FD939A'},
                {name: '200', color: '#FFBEC2'},
                {name: '100', color: '#FFEDEF'}
            ]
            },
        { swatch: 'Orange', colors: 
            [
                {name: '900', color: '#331D06'},
                {name: '800', color: '#663B11'},
                {name: '700', color: '#995A23'},
                {name: '600', color: '#CC7A3C'},
                {name: '500', color: '#f69b5a'},
                {name: '400', color: '#FFB177'},
                {name: '300', color: '#FFC799'},
                {name: '200', color: '#FFDEC1'},
                {name: '100', color: '#FFF6EE'}
            ]
            },
        { swatch: 'Yellow', colors: [
            {name: '900', color: '#332A02'},
            {name: '800', color: '#66520B'},
            {name: '700', color: '#99781B'},
            {name: '600', color: '#CC9B32'},
            {name: '500', color: '#f8bd4f'},
            {name: '400', color: '#FFCF6E'},
            {name: '300', color: '#FFE092'},
            {name: '200', color: '#FFEEBD'},
            {name: '100', color: '#FFFBED'}
        ]
        },
        { swatch: 'Grass', colors: [
            {name: '900', color: '#153300'},
            {name: '800', color: '#2C6500'},
            {name: '700', color: '#428D06'},
            {name: '600', color: '#5AAF15'},
            {name: '500', color: '#72cb2a'},
            {name: '400', color: '#91E052'},
            {name: '300', color: '#B2F07F'},
            {name: '200', color: '#D2FAB2'},
            {name: '100', color: '#F3FFEB'}
        ]
        },
        { swatch: 'Green', colors: [
            {name: '900', color: '#002E11'},
            {name: '800', color: '#005522'},
            {name: '700', color: '#007633'},
            {name: '600', color: '#009044'},
            {name: '500', color: '#05a455'},
            {name: '400', color: '#3BC27C'},
            {name: '300', color: '#75DBA3'},
            {name: '200', color: '#B0EECA'},
            {name: '100', color: '#EBFCF1'}
        ]
        },
        { swatch: 'Teal', colors: [
            {name: '900', color: '#0F3133'},
            {name: '800', color: '#225F61'},
            {name: '700', color: '#39888C'},
            {name: '600', color: '#53AFB2'},
            {name: '500', color: '#72d1d5'},
            {name: '400', color: '#8DE1E4'},
            {name: '300', color: '#ABEEF0'},
            {name: '200', color: '#CCF7F9'},
            {name: '100', color: '#F1FEFE'}
        ]
        },
        { swatch: 'Cyan', colors: [
            {name: '900', color: '#003133'},
            {name: '800', color: '#085D66'},
            {name: '700', color: '#168699'},
            {name: '600', color: '#2BACCC'},
            {name: '500', color: '#47cdf5'},
            {name: '400', color: '#67DEFF'},
            {name: '300', color: '#8EECFF'},
            {name: '200', color: '#BAF6FF'},
            {name: '100', color: '#ECFDFF'}
        ]
        },
        { swatch: 'Blue', colors: [
            {name: '900', color: '#001D33'},
            {name: '800', color: '#063B66'},
            {name: '700', color: '#155A99'},
            {name: '600', color: '#2A7ACC'},
            {name: '500', color: '#479aff'},
            {name: '400', color: '#67B0FF'},
            {name: '300', color: '#8DC7FF'},
            {name: '200', color: '#B9DEFF'},
            {name: '100', color: '#ECF7FF'}
        ]
        },
        { swatch: 'Violet', colors: [
            {name: '900', color: '#170F33'},
            {name: '800', color: '#312466'},
            {name: '700', color: '#4F3E99'},
            {name: '600', color: '#705CCC'},
            {name: '500', color: '#9580ff'},
            {name: '400', color: '#A996FF'},
            {name: '300', color: '#BFB0FF'},
            {name: '200', color: '#D8CFFF'},
            {name: '100', color: '#F5F2FF'}
        ]
        },
        { swatch: 'Purple', colors: [
                {name: '900', color: '#260F33'},
                {name: '800', color: '#4C2466'},
                {name: '700', color: '#733E99'},
                {name: '600', color: '#995CCC'},
                {name: '500', color: '#bf80ff'},
                {name: '400', color: '#CE96FF'},
                {name: '300', color: '#DCB0FF'},
                {name: '200', color: '#EBCFFF'},
                {name: '100', color: '#FAF2FF'}
            ]
        },
    { swatch: 'Pink', colors: 
            [
                {name: '900', color: '#33132D'},
                {name: '800', color: '#662958'},
                {name: '700', color: '#934381'},
                {name: '600', color: '#BC61A8'},
                {name: '500', color: '#e283cd'},
                {name: '400', color: '#EE9ADC'},
                {name: '300', color: '#F7B4E8'},
                {name: '200', color: '#FDD2F3'},
                {name: '100', color: '#FFF3FC'}
            ]
        },
    { swatch: 'Gray', colors: 
            [
                {name: '900', color: '#242424'},
                {name: '800', color: '#484848'},
                {name: '700', color: '#6B6B6B'},
                {name: '600', color: '#8F8F8F'},
                {name: '500', color: '#b3b3b3'},
                {name: '400', color: '#C5C5C5'},
                {name: '300', color: '#D6D6D6'},
                {name: '200', color: '#E7E7E7'},
                {name: '100', color: '#F9F9F9'}
            ]
        },
    { swatch: 'Slate', colors: 
            [
                {name: '900', color: '#1E1F23'},
                {name: '800', color: '#3D3E46'},
                {name: '700', color: '#5D5E68'},
                {name: '600', color: '#7D7E89'},
                {name: '500', color: '#9d9eaa'},
                {name: '400', color: '#B3B4BE'},
                {name: '300', color: '#C9CAD2'},
                {name: '200', color: '#E0E0E6'},
                {name: '100', color: '#F7F7F9'}
            ]
        },
    { swatch: 'Mist', colors: 
            [
                {name: '900', color: '#1F2528'},
                {name: '800', color: '#3F4A4F'},
                {name: '700', color: '#616F76'},
                {name: '600', color: '#83939B'},
                {name: '500', color: '#a6b7bf'},
                {name: '400', color: '#B9C8CF'},
                {name: '300', color: '#CDD9DF'},
                {name: '200', color: '#E2E9ED'},
                {name: '100', color: '#F7FAFB'}
            ]
        },
       
        ];

    let palette2 = [
        { swatch: 'Red', colors: 
            [
        {name: "0", color: "#ffeaec"},
        {name: "10", color: "#fdbdc2"},
        {name: "20", color: "#f89198"},
        {name: "30", color: "#f06c74"},
        {name: "40", color: "#e44e58"},
        {name: "50", color: "#d0313c"},
        {name: "60", color: "#b71c27"},
        {name: "70", color: "#970e17"},
        {name: "80", color: "#73060d"},
        {name: "90", color: "#4d0207"}
    ]
        }
    ]    
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

{#each palette2 as swatch}
    <div>
        <!-- <h1>{swatch.swatch}</h1> -->
        <section>
            {#each swatch.colors as {name, color}}
                <Swatch name="{swatch.swatch}-{name}" color={color} />
            {/each}
        </section>
    </div>
{/each}
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
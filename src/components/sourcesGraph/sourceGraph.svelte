<script>
    import { sourcesData } from "../../../data/sources_data";
    import SourceCountry from "./sourceCountry/sourceCountry.svelte";

    console.log(sourcesData);

    const rbs = Object.keys(sourcesData);

    
    function sortCountries(countryList){
        let sortedCountries = countryList.sort((a, b) => {
            let total_a = a["Household application"] + a["Other"] + a["Renewable general"] + a["Solar"] + a["Thermal"]
            let total_b = b["Household application"] + b["Other"] + b["Renewable general"] + b["Solar"] + b["Thermal"]
            return (total_a > total_b) ? -1 : +1
        })
        return sortedCountries;
    }

</script>

<div class="title">
    <h2> Overview of UNDP Solutions </h2>
    <p>
        The following chart shows the solutions mapped in different countries. 
        Colours indicate the type of energy the solution deals with. 
    </p>
</div>

<div class="graph-container">
    {#each rbs as rb }
        <h2> {rb} </h2>
        <div class="rb-container {rb}">
            {#each sortCountries(sourcesData[rb]) as country}
                <SourceCountry country={country} />
            {/each}
        </div>
    {/each}
</div>


<style>
    .title h2{
        font-family: "Roboto";
        font-size: 36px;
        letter-spacing: -1px;
        margin: 0;
        margin-bottom: 8px;
    }

    .title p{
        font-family: "Roboto";
        font-size: 16px;
        color: #222;
        max-width: 54ch;
        margin: 0;
    }

    .graph-container h2{
        font-family: 'Roboto';
        font-size: 28px;

        max-width: 50%;
        border-bottom: 1px solid #999;
    }

    .rb-container{
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;

        max-width: 800px;
    }
</style>
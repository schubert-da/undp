<script>
    import { sourcesData } from "../../../data/sources_data";
    import SourceCountry from "./sourceCountry/sourceCountry.svelte";

    console.log(sourcesData);

    const rbs = Object.keys(sourcesData);

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
        <div class="rb-container {rb}">
            <h2> {rb} </h2>
            {#each sourcesData[rb] as country}
                <SourceCountry country={country} />
            {/each}
        </div>
    {/each}
</div>


<style>
    .title h2{
        font-family: "Roboto Condensed";
        font-size: 36px;
        margin: 0;
        margin-bottom: 15px;
    }

    .title p{

    }
</style>
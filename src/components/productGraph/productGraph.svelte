<script>
    import { productData } from "../../../data/product_data";
    import ProductLegend from "./productLegend/productLegend.svelte";
    import ProductRb from "./productRB/productRB.svelte";


    const rbs = [
        "Africa",
        "Arab States",
        "Asia and Pacific",
        "Europe and the Commonwealth",
        "Latin American Countries"
    ]

</script>

<div class="title">
    <h2> The Road to Sustainability </h2>
    <p>
        <span class="italic">Since the beginning of time, people have been dreaming up ways to make life better for themselves and those around them, but too often their ideas get lost in a noisy world...</span>
        <br><br>
        As seen in the graph below, solutions captured by the UNDP labs often are still in the <b>prototype</b>( <span class="rect rect-proto"></span> ) stage where their <b>feasibility and scalability is still unknown</b>. Only 35% of solutions were tagged as <b>products</b>( <span class="rect rect-prod"></span> ) which were ready to scale to the masses. 
        <br><br>
        Only through the sharing of knowledge and resources are these grassroot solutions able to thrive. Those that are willing to train others in using and replicating their solutions( <span class="rect rect-proto"><span class="inner-rect"></span></span>, <span class="rect rect-prod"><span class="inner-rect"></span></span> ) are also shown in the graphic.
    </p>
</div>

<ProductLegend/>

<div class="graph-container">
    {#each rbs as rb }
        <div class="rb-container {rb}">
            <ProductRb rbData={productData.filter( d => d["rb"] === rb)} />
        </div>
   
    {/each}
</div>

<style>
    .title{
        margin-bottom: 20px;
    }

    .title h2{
        font-family: "Roboto";
        font-size: 36px;
        letter-spacing: -1px;
        margin: 0;
        margin-bottom: 24px;
    }

    .title p{
        font-family: "Roboto";
        font-size: 16px;
        color: #222;
        max-width: 54ch;
        margin: 0;
    }

    span.italic{
        font-family: "Roboto Condensed";
        font-size: 18px;
        font-style: italic;
        letter-spacing: -0.3px;
        color: #444;
    }

    .rect{
        width: 16px;
        min-width: 16px;
        height: 16px;
         
        border: 2px solid #666;
        border-radius: 2px;

        vertical-align: bottom;
        display: inline-flex;
        align-items: center;
        justify-content: center;
    }

    .inner-rect{
        display: block;
        width: 65%;
        height: 65%;

        background-color: #efefef;
        border: 1px solid #666;
    }

    .rect-prod{
        background-color: #509DBA;
    }

    .rect-proto{
        background-color: #666;
    }

    .rb-container{
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;

        max-width: 800px;
    }
</style>
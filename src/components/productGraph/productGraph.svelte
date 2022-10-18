<script>
    import { productData } from "../../../data/product_data";
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
        The following chart shows the solutions mapped in different countries. 
        Colours indicate the type of energy the solution deals with. 
    </p>
</div>


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
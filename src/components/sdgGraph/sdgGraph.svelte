<script>
    import SdgRb from "./sdgRB/sdgRB.svelte";
    import SdgLegend from "./sdgLegend/sdgLegend.svelte";
    import { sdgData, sdgLabels } from "../../../data/sdg_data";


    let chosenSDGs = [1,2,3,4,5];
</script>

<div class="title">
    <h2> Same problem, different solutions </h2>
    <p>
        Even when working towards the same goals, in different regions  
    </p>
</div>

<SdgLegend/>

<div class="graph-container">

    {#each chosenSDGs as sdg }
        <div class="sdg-container">
            <h2 class="sdg-title"> { sdgLabels[sdg] } </h2>
            <SdgRb rbData = {sdgData.filter( d => d.sdg === sdg )}/>
        </div>
    {/each} 

</div>


<style>
    .title{
        margin-bottom: 24px;
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

    .sdg-container{
        padding: 30px 20px 30px 10px;
        margin-top: 25px;
        margin-bottom: auto;
        margin-right: 10px;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;

        border: 1px solid #999;
        border-radius: 5px;
        width: fit-content;
        max-width: 700px;

        position: relative;
    }

    .sdg-container .sdg-title{
        padding: 0px 5px;
        font-family: 'Roboto';
        font-weight: bold;
        background-color: #fff;
        margin: 0;
        padding: 2px 10px;
        border: none;

        position: absolute;
        left: 15px;
        top: -16px;
    }

    .graph-container h2{
        font-family: 'Roboto';
        font-size: 28px;

        border-bottom: 1px solid #999;
    }
</style>
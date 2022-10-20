<script>
    import SdgRb from "./sdgRB/sdgRB.svelte";
    import SdgLegend from "./sdgLegend/sdgLegend.svelte";
    import { sdgData, sdgLabels } from "../../../data/sdg_data";


    let chosenSDGs = [7,11,9,13,12];
</script>

<div class="title">
    <h2> Same problem, different solutions </h2>
    <p>
        The <b>Sustainable Development Goals</b>(SDGs) are the blueprint to achieve a better and more sustainable future for all. They address the global challenges we face, including poverty, inequality, climate change, peace, justice, etc.
        <br><br>
        Such problems can't be solved with one unified solution by someone sitting behind a desk hundreds of miles away - the <b>people closest to the problem have the most knowledge about it</b>.
        <br><br><br>
        Solutions for the same SDG take on a very different nature based on the unique challenges of the locale. We see how the types of solutions tackling the same SDG vary across different regional bureaus.
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
        margin-bottom: 24px;
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
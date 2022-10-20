<script>

</script>

<div class="legend">
    <div class="legend-title">Energy categorisation </div>
    <div class="legend-item">
        <div class="rect rect-household"></div>
        <span class="legend-item-text"> Household applications <br> <span class="light">Solutions that address problems at household level. eg energy meters, battery packs.</span></span>
    </div>

    <div class="legend-item">
        <div class="rect rect-solar"></div>
        <span class="legend-item-text"> Solar</span>
    </div>

    <div class="legend-item">
        <div class="rect rect-thermal"></div>
        <span class="legend-item-text"> Thermal <br> <span class="light">Wood, coal, biomass-based stoves/processors, geo-thermal, etc.</span></span>
    </div>

    <div class="legend-item">
        <div class="rect rect-renewable"></div>
        <span class="legend-item-text"> Renewable general <br> <span class="light">Summary term for solutions with an educational purpose improved resource/energy management, and green urban mobility.</span></span>
    </div>

    <div class="legend-item">
        <div class="rect rect-other"></div>
        <span class="legend-item-text"> Other <br> <span class="light">Includes less prominent categories like wind, mechanical, chemical, etc.</span></span>
    </div>
</div>

<style>
    .legend{
        padding: 15px;
        border: 1px solid #222;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;

        border: 1px solid #999;
        border-radius: 5px;
        max-width: 400px;

        /* margin-bottom: 40px; */
    }

    .legend-title{
        font-family: 'Roboto';
        font-weight: bold;
        font-size: 20px;
        margin-bottom: 8px;
    }
    
    .legend-item{
        display: flex;
        flex-direction: row;
    }
    
    .legend-item:not(:last-of-type){
        margin-bottom: 6px;
    }

    .legend-item-text{
        padding-left: 10px;
        padding-top: 6px;
        font-family: 'Roboto';
        font-weight: bold;
        font-size: 17px;
    }

    .legend-item-text .light{
        font-weight: 400;
        font-size: 16px;
    }

    .rect{
        width: 23px;
        min-width: 23px;
        height: 23px;
        margin: 2px;

        background-color: #666;
        border: 1px solid #222;
        border-radius: 2px;
    }

    .rect-household{
        background-color: #509DBA;
    }

    .rect-solar{
        background-color: #222;
    }

    .rect-thermal{
        background-color: #666;
    }

    .rect-renewable{
        background-color: #ECC86C;
    }

    .rect-other{
        background-color: #E0E0E0;
    }
</style>
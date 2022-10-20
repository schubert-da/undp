<script>

</script>

<div class="legend">
    <div class="legend-item">
        <div class="rect rect-household"></div>
        <span class="legend-item-text"> Household applications</span>
    </div>

    <div class="legend-item">
        <div class="rect rect-solar"></div>
        <span class="legend-item-text"> Solar</span>
    </div>

    <div class="legend-item">
        <div class="rect rect-thermal"></div>
        <span class="legend-item-text"> Thermal</span>
    </div>

    <div class="legend-item">
        <div class="rect rect-renewable"></div>
        <span class="legend-item-text"> Renewable general</span>
    </div>

    <div class="legend-item">
        <div class="rect rect-other"></div>
        <span class="legend-item-text"> Other</span>
    </div>
</div>

<style>
    .legend{
        padding: 12px;
        border: 1px solid #222;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;

        border: 1px solid #999;
        border-radius: 5px;
        width: fit-content;

        display: flex;
        flex-direction: row;
    }
    
    .legend-item{
        display: flex;
        flex-direction: row;
        align-items: center;
    }
    
    .legend-item:not(:last-of-type){
        margin-right: 14px;
    }

    .legend-item-text{
        padding-left: 4px;
        padding-top: 6px;
        font-family: 'Roboto';
        font-weight: bold;
        font-size: 16px;
    }

    .rect{
        width: 20px;
        height: 20px;
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
        background-color: #eaeaea;
    }
</style>
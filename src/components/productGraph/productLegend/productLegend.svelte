<script>

</script>

<div class="legend">
    <div class="legend-title"> How ready is the solution to scale? </div>
    <div class="legend-item">
        <div class="rect rect-prod"></div>
        <span class="legend-item-text"> Solution is a product <span class="light"> - proved to be scalable </span></span>
    </div>

    <div class="legend-item">
        <div class="rect rect-prod">
            <div class="inner-rect"></div>
        </div>
        <span class="legend-item-text"> Solution is a product <span class="light">and solution holder is <b>able to train</b> others</span> </span>
    </div>

    <div class="legend-item">
        <div class="rect rect-proto"></div>
        <span class="legend-item-text"> Solution is a prototype <span class="light"> - unproven to be scalable or feasible </span></span>
    </div>

    <div class="legend-item">
        <div class="rect rect-proto">
            <div class="inner-rect"></div>
        </div>
        <span class="legend-item-text"> Solution is a prototype <span class="light">and solution holder is <b>able to train</b> others</span> </span>
    </div>

    <div class="legend-item">
        <div class="rect rect-unknown"></div>
        <span class="legend-item-text"> Unknown </span>
    </div>
</div>

<style>
    .legend{
        padding: 15px;
        border: 1px solid #222;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;

        border: 1px solid #999;
        border-radius: 5px;
        width: 400px;
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
        font-size: 16px;
    }

    .legend-title{
        font-family: 'Roboto';
        font-weight: bold;
        font-size: 20px;
        margin-bottom: 8px;
    }

    .legend-item-text .light{
        font-weight: 400;
        font-size: 16px;
    }

    .rect{
        width: 25px;
        min-width: 25px;
        height: 25px;
        margin: 2px;

        background-color: #666;
        border: 1px solid #222;
        border-radius: 2px;

        display: flex;
        align-items: center;
        justify-content: center;
    }

    .inner-rect{
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

    .rect-unknown{
        background-color: #E0E0E0;
    }
</style>
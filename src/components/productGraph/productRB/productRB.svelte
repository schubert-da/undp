<script>
    export let rbData;

    console.log("rbData");
    console.log(rbData);
</script>

<div class="rb-container">
    <div class="title">
        {rbData[0]["rb"]}
    </div>

    <div class="rect-container">
        {#each rbData as soln}
            <div class={"rect prod-"+soln["product"]+" proto-"+soln["prototype"]}>
                {#if soln["able_to_train"] === true }
                    <div class="inner-rect">
                    </div>
                {/if}
            </div>
        {/each}
    </div>
</div>

<style>
    .rb-container{
        margin-top: 25px;
        margin-bottom: auto;
        margin-right: 10px;
        padding-top: 25px;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;

        border: 1px solid #999;
        border-radius: 5px;
        width: fit-content;

        position: relative;
    }

    .title{
        padding: 0px 5px;
        font-family: 'Roboto';
        font-size: 28px;
        font-weight: bold;
        background-color: #fff;

        position: absolute;
        left: 15px;
        top: -12px;
    }
    

    .rect-container{
        display: flex;
        flex-wrap: wrap;
        width: 520px;
        margin: 12px 10px 10px 10px;
    }

    .rect{
        width: 30px;
        height: 30px;
        margin: 2.2px;

        background-color: #666;
        border: 1px solid #222;
        border-radius: 2px;

        display: flex;
        align-items: center;
        justify-content: center;
    }

    .inner-rect{
        width: 70%;
        height: 70%;

        background-color: #efefef;
        border: 1px solid #666;
    }

    .prod-true{
        background-color: #509DBA;
    }

    .proto-true{
        background-color: #666;
    }

    .proto-false.prod-false{
        background-color: #efefef;
    }

</style>
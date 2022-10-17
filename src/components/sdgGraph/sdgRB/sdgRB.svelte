<script>
    export let rbData;

    let barWidth = 300;
    console.log(rbData);
</script>

{#each rbData as rb }
    <div class="rb-container">
        <div class="title">
            {rb.rb}
        </div>

        <div class="bar">
            <div class="rect rect-household" 
                style={"width:"+(rb["Household application"]*barWidth)+"px"}>
            </div>
            
            <div class="rect rect-solar" 
                style={"width:"+(rb["Solar"]*barWidth)+"px"}>
            </div>

            <div class="rect rect-thermal" 
                style={"width:"+(rb["Thermal"]*barWidth)+"px"}>
            </div>

            <div class="rect rect-renewable" 
                style={"width:"+(rb["Renewable general"]*barWidth)+"px"}>
            </div>

            <div class="rect rect-other" 
                style={"width:"+(rb["Other"]*barWidth)+"px"}>
            </div>

        </div>
    </div>
{/each}


<style>
    .rb-container{
        display: flex;
        flex-direction: row;
        align-items: center;
        margin-bottom: 10px;
    }

    .rb-container .title{
        width: 240px;
        font-family: 'Roboto';
        font-weight: bold;
        text-align: end;
        margin-right: 16px;
    }

    .rb-container .bar{
        width: 300px;
        height: 26px;
        /* background-color: #ddd; */
        border: 1px solid #666;
        display: flex;
    }

    .rb-container .bar .rect{
        height: 100%;
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
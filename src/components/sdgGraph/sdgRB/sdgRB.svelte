<script>
    export let rbData;

    console.log(rbData);
</script>

{#each rbData as rb }
    <div class="rb-container">
        <div class="title">
            {rb.rb}
        </div>

        <div class="rect-container">
            rect
        </div>
    </div>
{/each}


<style>
    .rb-container{
        
    }

    .rect-container{
        display: flex;
        flex-wrap: wrap;
        width: 220px;
        margin: 12px 10px 10px 10px;
    }

    .rect{
        width: 30px;
        height: 30px;
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
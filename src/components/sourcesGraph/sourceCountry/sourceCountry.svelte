<script>
    export let country;

</script>

<div class="country-container">
    <div class="title">
        {country.country}
    </div>
    <div class="rect-container">
        {#each  Array(country["Household application"]) as _, i}
            <div class="rect rect-household"></div>
        {/each}

        {#each  Array(country["Solar"]) as _, i}
            <div class="rect rect-solar"></div>
        {/each}

        {#each  Array(country["Thermal"]) as _, i}
            <div class="rect rect-thermal"></div>
        {/each}

        {#each  Array(country["Renewable general"]) as _, i}
            <div class="rect rect-renewable"></div>
        {/each}

        {#each  Array(country["Other"]) as _, i}
            <div class="rect rect-other"></div>
        {/each}

    </div>
</div>

<style>

    .country-container{
        margin-bottom: 20px;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;

        border: 1px solid #999;
        border-radius: 5px;
        max-width: 250px;

        position: relative;
    }

    .title{
        padding: 0px 5px;
        font-family: 'Roboto';
        font-weight: bold;
        background-color: #fff;

        position: absolute;
        left: 15px;
        top: -12px;
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
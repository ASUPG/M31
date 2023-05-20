<script>
    export let sdkname
    export let sdklogo
    export let status
</script>
{#if status == "available"}
<div class="sdk-wrapper available">
    <div class="sdk">
        <img src="{sdklogo}" alt="{sdkname}">
        <span class="name">{sdkname}</span>
    </div>
</div>
{:else if status == "working"}
<div class="sdk-wrapper available working">
    <div class="sdk">
        <img src="{sdklogo}" alt="{sdkname}">
        <span class="name">{sdkname}</span>
    </div>
</div>

{:else if status == "not-available"}
<div class="sdk-wrapper not-available">
    <div class="sdk">
        <img src="{sdklogo}" alt="{sdkname}">
        <span class="name">{sdkname}</span>
    </div>
</div>
{/if}
<style lang="scss">
    .sdk{
        display: grid;
        grid-template-columns: 1fr 3fr;
        align-items: center;
        background-color: var(--secbackground);
        width:168px;
        height: 68px;
        margin: 0;
        border-radius: 20px;
        img{
            aspect-ratio: 1/1;;
            width: 40px;
            margin:5px;
        }
        span{
            width:100%;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100%;
        }
    }
    .sdk-wrapper{
        box-sizing: border-box;
        padding: 0;
        height: 70px;
        width:170px;
        border-radius: 20px;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-right: 4px;
        margin-left: 4px;
    }
    .available{
        background-image: linear-gradient(45deg, lime, green);
    }
    .working{
        background-image: linear-gradient(45deg, #0869f9, blue);
    }
    .not-available{
        background-image: linear-gradient(45deg, #fdb706, red);
    }
</style>

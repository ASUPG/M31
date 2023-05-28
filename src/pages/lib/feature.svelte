<script>
export let name
export let description
</script>
<div class="gradient-border">
    <div class="feature">
        <h3 class="title">{name}</h3>
        <p>{description}</p>
    </div>
</div>
<style lang="scss">
    .gradient-border{
        width: 90%;
        height: auto;
        border-radius: 10px;
        color: white !important;
        display: flex;
        align-items: center;
        justify-content: center;
        background-image: linear-gradient(to right,red,yellow, lime,green,lightblue, blue, violet, purple);
    }
    .feature {
        height: calc(100% - 2px);
        width: calc(100% - 2px);
        border-radius: 10px;;
        background-color: var(--secbackground);
        color: white !important;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        .title{
            margin: 10px 0px 0px 10px;
        }
        p{
            margin: 10px 0px 10px 10px;
            font-size: small;
            color: rgb(184, 184, 184);
        }
    }
</style>
<script>
  export let name;
</script>

<h1 class="head">{name} <!--is 
<span>Fast</span>
<span>Flexible</span>
<span>Scalable</span>
<span>Easy to use</span>
<span></span>-->
</h1>

<style lang="scss">
  .head {
    width: 100%;
    height: 55px;
    display: flex;
    flex-direction: column;
    font-size: 8vw;
    align-items: center;
    color: var(--font-color) !important;
    color: white;
    animation: load 1s var(--animation-curve);
    span{
        color: rgb(0, 205, 0);
    }
  }
  @media only screen and (min-width: 627px) {
    .head {
      font-size: 50.16px !important;
    }
  }
</style>

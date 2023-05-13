<script>
    import Icon from "./moreicon.svelte"
</script>
<nav class="navbar">
    <h1 class="brandlabel">Cosmic Horizon</h1>
    <ul class="links">
        <li class="link"><a href="/">Home</a></li>
        <li class="link"><a href="/docs/">Docs</a></li>
        <li class="link"><a href="/about">About Us</a></li>
        <li class="link"><a href="/contact">Contact US</a></li>
    </ul>
    <div class="icon">
        <button type="button" class="moreicon">
            <Icon />
        </button>
        <a href="https://github.com/TheUtkarsh8939/M31DB">
            <img class="github" src="github.svg" alt="Github">
        </a>
    </div>
</nav>
<style lang="scss">
    @mixin flex-align-center {
        display: flex;
        align-items: center;
        height: 100%;
        width: 100%;
    }
    .navbar{
        width: 100%;
        height: 125px;
        display: grid;
        grid-template-columns: 20% 60% 20%;
        grid-template-rows: 100%;
        align-items: center;
        font-family: sans-serif;
        background-color: var(--mainbackground);
        color: var(--font-color);
        border-bottom: 1px solid gray;
        position: fixed;
        box-shadow: 5px 5px 5px black, 10px 10px 10px #020023;
        .brandlabel {
            margin-left: 30px;
            font-size: 6vw;
            @include flex-align-center();
        }
    }
    .icon{
        @include flex-align-center();
        margin-left: 70%;
        .github{
            height: 40px;
            width: 40px;
        }
    }

    .links {
        display: flex;
        list-style: none;
        @include flex-align-center();
        justify-content: space-evenly;
        width: 60%;
        align-self: center;
        justify-self: center;
        .link{
            a{
                color: var(--font-color) !important;
                text-decoration: none;
                font-size: 18px;
            }
        }
    }
    .moreicon{
        background-color: transparent;
        border: transparent;
        display: none;
    }
    /*Responsiveness */
    @media only screen and (max-width: 772px) {
        .links{
            display: none;
        }
        .github{
            display: none;
        }
        .moreicon{
            display: flex;
            align-items: center;
            justify-content: center;
            widows: 100%;
            height: 100%;
        }
        .icon{
            margin-left: 60%;
        }
        .navbar{
            grid-template-columns: 80% 20%;
        }
    }
    @media only screen and (min-width: 673px) {
        .brandlabel{
            font-size: 40px !important;
        }
    }
</style>
<script>
    import Icon from "./moreicon.svelte"
    export const name = "AndromedaDB"
    let dropcount = 0
    function dropdown(){
          dropcount+=1
          if (dropcount%2 != 0){
              document.getElementById("dropdown").style.display = "flex";
          }
          else{
            document.getElementById("dropdown").style.display = "none"
          }
    }
</script>
<div class="nav-wrapper" style="position:fixed;">
    <nav class="navbar">
        <h1 class="brandlabel">{name}</h1>
        <ul class="links">
            <li class="link"><a href="/">Home</a></li>
            <li class="link"><a href="/docs/">Docs</a></li>
            <li class="link"><a href="/about">About Us</a></li>
            <li class="link"><a href="/contact">Contact US</a></li>
        </ul>
        <div class="icon">
            <button on:click={dropdown} type="button" class="moreicon">
                <Icon />
            </button>
            <a href="https://github.com/TheUtkarsh8939/M31DB">
                <img class="github" src="github.svg" alt="Github">
            </a>
        </div>
    </nav>
</div>
<div id="dropdown" style="position:absolute;">
    <div class="dropul">
        <span class="drop-item">Home</span>
        <span class="drop-item">Docs</span>
        <span class="drop-item">About Us</span>
        <span class="drop-item">Contact Us</span>
        <span class="drop-item">Github</span>
    </div>
</div>
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
        position: fixed;
        .brandlabel {
            margin-left: 30px;
            font-size: 6vw;
            @include flex-align-center();
        }
    }
    .nav-wrapper {
        width:100%;
        height:127.5px;
        background-image: linear-gradient(to right, #46ea00, #0026ff);
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
    #dropdown{
        margin-top: 127.5px;
        position: absolute;
        background-color: #2d2d2d;
        width: 100%;
        display: none;
        .dropul{
            list-style: none;
            z-index:2;
            width:100%;
            display:flex;
            flex-direction: column;
            align-items: center;
            height: auto;
            span{
                display:flex;
                align-items: center;
                justify-content: center;
                border: 1px solid #3f3e3e;
                padding: 10px;
                width:100%;
            }
        }
    }
    body{
        position: absolute;
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
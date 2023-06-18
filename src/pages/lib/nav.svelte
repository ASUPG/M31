<script>
  import Icon from "./moreicon.svelte";
  export let name;
  let dropcount = 0;
  function dropdown() {
    dropcount += 1;
    if (dropcount % 2 != 0) {
      document.getElementById("sidebar").style.transform = "translateX(0px)";
    } else {
      document.getElementById("sidebar").style.transform = "translateX(400px)";
    }
  }
</script>

<div class="nav-wrapper" style="position:fixed;">
  <nav class="navbar">
    <h1 class="brandlabel">{name}</h1>
    <div class="icon">
      <button on:click={dropdown} type="button" class="moreicon">
        <Icon />
      </button>
    </div>
  </nav>
</div>
<sidebar id="sidebar" style="position:absolute;">
  <div class="head">
    <h1>M31DB</h1>
    <a href="https://github.com/ASUPG/M31DB" target="_blank"><img src="github.svg" alt="" /></a>
  </div>
  <div class="sideul">
    <a target="_blank" href="/" class="drop-item">Home</a>
    <a target="_blank" href="#" class="drop-item">Docs</a>
    <a target="_blank" href="#" class="drop-item">Report an Issue</a>
    <a target="_blank" href="#" class="drop-item">Feedback</a>
    <a target="_blank" href="#" class="drop-item">Donate</a>
  </div>
  <h1>Contributing</h1>
  <div class="sideul">
    <a target="_blank" href="/contribution/licensing" class="drop-item">License</a>
    <a target="_blank" href="/contribution/contribution" class="drop-item">Contribution Guidelines</a>
    <a target="_blank" href="/contribution/code-of-conduct" class="drop-item">Code of Conduct</a>
  </div>
  <h1>Community</h1>
  <div class="sideul">
    <a target="_blank" href="https://www.reddit.com/r/M31DB/" class="drop-item">Reddit</a>
    <a target="_blank" href="https://github.com/ASUPG/M31DB/discussions" class="drop-item">Github</a>
  </div>
</sidebar>

<style lang="scss">

  @mixin flex-align-center {
    display: flex;
    align-items: center;
    height: 100%;
    width: 100%;
  }
  .navbar {
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
    width: 100%;
    height: 127.5px;
    background-image: linear-gradient(to right, #46ea00, #0026ff);
  }
  .icon {
    @include flex-align-center();
    margin-left: 70%;
  }

  .moreicon {
    background-color: transparent;
    border: transparent;
    display: none;
  }
  #sidebar {
    transform: translateX(400px);
    z-index: 25;
    margin-top: 127.5px;
    position: absolute;
    background-color: rgb(11, 11, 11);
    box-shadow: 10px 10px 10px 0px black;
    width: 325px;
    display: flex;
    transition: 2s all;
    margin-left: calc(100% - 325px);
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    .head {
      width: 100%;
      display: grid;
      grid-template-columns: 1fr 1fr;
      align-items: center;
      justify-content: center;
      h1{
        align-items: center;
        width: 100%;
        display: flex;
        justify-content: center;
      }
      a{
          justify-self: self-end;
      }
    }
    .sideul {
      margin-top: 30px;
      list-style: none;
      width: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
      height: auto;
      gap: 10px;
      .drop-item {
        display: flex;
        align-items: center;
        justify-content: center;
        border-bottom: 1px solid #3f3e3e;
        padding: 10px;
        width: 305px;
        transition: all 0.5s;
        text-decoration: none;
        color:white;
        &:hover {
          color: rgb(255, 251, 251);
          cursor: pointer;
          border-bottom: 1px solid #a3a3a3;
        }
      }
    }
  }
  .moreicon {
    display: flex;
    align-items: center;
    justify-content: center;
    widows: 100%;
    height: 100%;
  }
  .icon {
    margin-left: 60%;
  }
  .navbar {
    grid-template-columns: 80% 20%;
  }

  @media only screen and (min-width: 673px) {
    .brandlabel {
      font-size: 40px !important;
    }
  }
</style>

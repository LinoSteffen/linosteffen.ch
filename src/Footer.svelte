<script lang="ts">
    export let setActivePage;
</script>

<footer class="footer">
    <div class="onefooter">
        <div class="top">
            <div class="socials">
                <a href="https://ch.linkedin.com/in/lino-steffen-2937631bb" target="_blank"><i class="fab fa-linkedin"></i></a>
                <a href="https://www.youtube.com/@linosteffen" target="_blank"><i class="fab fa-youtube"></i></a>
                <a href="https://www.instagram.com/lino.steffen/" target="_blank"><i class="fab fa-instagram"></i></a>
                <a href="https://www.facebook.com/lino.steffen.33" target="_blank"><i class="fab fa-facebook"></i></a>
                <a href="https://www.tiktok.com/@lino.steffen" target="_blank"><i class="fab fa-tiktok"></i></a>
                <a href="https://github.com/LinoSteffen" target="_blank"><i class="fab fa-github"></i></a>
            </div>
        </div>
        <div class="bottom">
            <div class="links">
                <!-- svelte-ignore a11y-click-events-have-key-events -->
                <div on:click={() => setActivePage('Home')}>Home</div>
                <!-- svelte-ignore a11y-click-events-have-key-events -->
                <div on:click={() => setActivePage('Impressum')}>Impressum</div>
            </div>
        </div>
    </div>
    <div class="copyrightdiv">
        <p class="copyrighttext">Lino Steffen © 2024</p>
    </div>
</footer>

<style>
    .footer {
        z-index: 8;
        position: relative;
        min-height: 9vh;
        bottom: 0;
        width: 100%;
        background-color: #000A14;
        color: white;
    }

    /* Footer Part One*/
    .onefooter {
        width: 100%;
        height: 20vh;
    }

    /* top - socials */
    .top {
        height: 40%;
        text-align: center;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    @media (min-width: 750px) {
        .top {
        margin-left: 10%;
        margin-right: 10%;
        }
    }

    .socials {
        width: 100%;
        padding-top: 25px;
        padding-bottom: 10px;
        margin: 0;
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        flex-wrap: wrap;
    }
    .socials > a {
        padding: 0;
        font-size: 25px;
        display:inline-block;
        text-align:center;
        color:inherit;
        opacity:0.7;
        transition: all ease 0.5s;
    }
    .socials > a:hover {
        opacity:1.0;
    }

    /* bottom - links to Pages */ 
    .bottom {
        height: 60%;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .links {
        width: 100%;
        font-family: sans-serif;
        padding: 0;
        list-style: none;
        text-align: center;
        font-size: 18px;
        line-height: 1.6;
        cursor: pointer;
    }
    .links > div {
        color:inherit;
        text-decoration:none;
        opacity:0.7;
        transition: all ease 0.5s;
    }
    .links > div:hover {
        opacity: 1;
    }
    
    /* Footer Part Two*/
    /* Copyright */
    .copyrightdiv {
        margin: 0;
        text-align:center;
        padding-top: 1px;
        padding-bottom: 8px;
    }
    .copyrighttext {
        font-size:13px;
        opacity: 0.7;
    }
</style>
<script>
    import Intersector from './lib/Intersecting.svelte'
    import Hoverable from './lib/Hoverable.svelte';
    import Title from './lib/Title.svelte';

    import { onMount } from "svelte";
    import Placeholder from './lib/Placeholder.svelte';

    let sponsors = [];

    let loaded = false;

    onMount(async () => {
        const response = await fetch("/sponsors.json");
        sponsors = await response.json();
    });

    function imageLoad() {
        loaded = true;
    }
</script>

<Placeholder />

<div id="title">
    <Title text="Lino Steffen" charCount="9" writedelay="30" writechardelay="15"/>
</div>

<!-- Generated with softr.io -->
<div class="main-interface-container">
    <img id="main-interface" width="100%" src="/background.jpeg" alt="Sunrise Background" on:load={imageLoad}/>

    <svg id="main-interface-wave-top" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 100" version="1.1">        
        <path class="shape-fill" d="M0,70L48,70C96,70,192,70,288,68.3C384,67,480,63,576,65C672,67,768,73,864,71.7C960,70,1056,60,1152,60C1248,60,1344,70,1440,76.7C1536,83,1632,87,1728,78.3C1824,70,1920,50,2016,41.7C2112,33,2208,37,2304,45C2400,53,2496,67,2592,65C2688,63,2784,47,2880,46.7C2976,47,3072,63,3168,61.7C3264,60,3360,40,3456,33.3C3552,27,3648,33,3744,41.7C3840,50,3936,60,4032,53.3C4128,47,4224,23,4320,11.7C4416,0,4512,0,4608,0C4704,0,4800,0,4896,3.3C4992,7,5088,13,5184,28.3C5280,43,5376,67,5472,75C5568,83,5664,77,5760,73.3C5856,70,5952,70,6048,66.7C6144,63,6240,57,6336,60C6432,63,6528,77,6624,68.3C6720,60,6816,30,6864,15L6912,0L6912,100L6864,100C6816,100,6720,100,6624,100C6528,100,6432,100,6336,100C6240,100,6144,100,6048,100C5952,100,5856,100,5760,100C5664,100,5568,100,5472,100C5376,100,5280,100,5184,100C5088,100,4992,100,4896,100C4800,100,4704,100,4608,100C4512,100,4416,100,4320,100C4224,100,4128,100,4032,100C3936,100,3840,100,3744,100C3648,100,3552,100,3456,100C3360,100,3264,100,3168,100C3072,100,2976,100,2880,100C2784,100,2688,100,2592,100C2496,100,2400,100,2304,100C2208,100,2112,100,2016,100C1920,100,1824,100,1728,100C1632,100,1536,100,1440,100C1344,100,1248,100,1152,100C1056,100,960,100,864,100C768,100,672,100,576,100C480,100,384,100,288,100C192,100,96,100,48,100L0,100Z"></path>
    </svg>
</div>
<svg id="main-interface-wave-bottom" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 100" version="1.1">
    <path class="shape-fill" d="M0,70L48,70C96,70,192,70,288,68.3C384,67,480,63,576,65C672,67,768,73,864,71.7C960,70,1056,60,1152,60C1248,60,1344,70,1440,76.7C1536,83,1632,87,1728,78.3C1824,70,1920,50,2016,41.7C2112,33,2208,37,2304,45C2400,53,2496,67,2592,65C2688,63,2784,47,2880,46.7C2976,47,3072,63,3168,61.7C3264,60,3360,40,3456,33.3C3552,27,3648,33,3744,41.7C3840,50,3936,60,4032,53.3C4128,47,4224,23,4320,11.7C4416,0,4512,0,4608,0C4704,0,4800,0,4896,3.3C4992,7,5088,13,5184,28.3C5280,43,5376,67,5472,75C5568,83,5664,77,5760,73.3C5856,70,5952,70,6048,66.7C6144,63,6240,57,6336,60C6432,63,6528,77,6624,68.3C6720,60,6816,30,6864,15L6912,0L6912,100L6864,100C6816,100,6720,100,6624,100C6528,100,6432,100,6336,100C6240,100,6144,100,6048,100C5952,100,5856,100,5760,100C5664,100,5568,100,5472,100C5376,100,5280,100,5184,100C5088,100,4992,100,4896,100C4800,100,4704,100,4608,100C4512,100,4416,100,4320,100C4224,100,4128,100,4032,100C3936,100,3840,100,3744,100C3648,100,3552,100,3456,100C3360,100,3264,100,3168,100C3072,100,2976,100,2880,100C2784,100,2688,100,2592,100C2496,100,2400,100,2304,100C2208,100,2112,100,2016,100C1920,100,1824,100,1728,100C1632,100,1536,100,1440,100C1344,100,1248,100,1152,100C1056,100,960,100,864,100C768,100,672,100,576,100C480,100,384,100,288,100C192,100,96,100,48,100L0,100Z"></path>
</svg>
<!-- Generated with softr.io -->

<div class="main-container-outer" style="margin-top: 0;">
    <div class="main-container-inner">
        <Intersector styleOnDefault="scale: 0.7;" styleOnIntersect="scale: 1;" transition="all ease 1s">
            <h1>Willkommen</h1>
        </Intersector>
        <Intersector styleOnDefault="scale: 0.7;" styleOnIntersect="scale: 1;" transition="all ease 1s">
            <p>Ich bin Lino Steffen</p>
        </Intersector>
        <Intersector styleOnDefault="scale: 0.7;" styleOnIntersect="scale: 1;" transition="all ease 1s">
            <p>Als <Hoverable text="Video Creator" gifsrc="/assets/hover/videocreator.gif" color="#FD5901" alt="gif Video Creator"/> und <Hoverable text="Fotograf" gifsrc="/assets/hover/photography.gif" color="#FD5901" alt="gif Fotograf"/> aus Bern verwandle ich deine Ideen in beeindruckende Bilder.</p>
        </Intersector>
        <Intersector styleOnDefault="scale: 0.7;" styleOnIntersect="scale: 1;" transition="all ease 1s">
            <p>Ob ein professionelles Video oder hochwertige Fotos, ich bin dein kreativer und zuverlässiger <Hoverable text="Partner" gifsrc="/assets/hover/partner.gif" color="#FD5901" alt="gif Partner"/>.</p>
        </Intersector>
        <Intersector styleOnDefault="scale: 0.7;" styleOnIntersect="scale: 1;" transition="all ease 1s">
            <p><Hoverable text="Kontaktiere" gifsrc="/assets/hover/telephone.gif" color="#FD5901" alt="gif Telephone"/> mich und lasse uns gemeinsam deine <Hoverable text="Geschichte" gifsrc="/assets/hover/history.gif" color="#FD5901" alt="gif Geschichte"/> erzählen.</p>         
        </Intersector>
        <Intersector styleOnDefault="scale: 0.7;" styleOnIntersect="scale: 1;" transition="all ease 1s">
            <img class="ls-icon" src=./LSwhite.png width="25" alt="Lino Steffen Icon">
        </Intersector>
    </div>
</div>
<div class="main-container-outer">
    <div class="main-container-inner">
        <Intersector styleOnDefault="scale: 0.7;" styleOnIntersect="scale: 1;" transition="all ease 1s">
            <h1>Partners in Success</h1>
        </Intersector>
        <Intersector styleOnDefault="scale: 0.7;" styleOnIntersect="scale: 1;" transition="all ease 1s">
            <div class="sponsor-list">
                {#each sponsors as sponsor}
                    <a href="{sponsor.lnk}">
                        <div class="sponsor-bx">
                            <img src="{sponsor.src}" alt="{sponsor.alt}" style="filter: invert({sponsor.invert});"/>
                        </div>
                    </a>
                {/each}
            </div>
        </Intersector>
        <Intersector styleOnDefault="scale: 0.7;" styleOnIntersect="scale: 1;" transition="all ease 1s">
            <img class="ls-icon" src=./LSwhite.png width="25" alt="Lino Steffen Icon">
        </Intersector>
    </div>    
</div>


<style>
    .importantword {
        color: #FD5901;
        font-weight: bold;
    }

    /* Title resizing */
    #title {
        z-index: 6;
        position: absolute;
        width: 100%;
        top: 30%;
        user-select: none;
        cursor: pointer;
        font-family: sans-serif;
        font-size: 8rem;
        font-weight: 600;
        transition: all linear 1s;
    }

    @media (max-width: 700px) {
        #title, .main-interface-container, .main-container-inner {
            margin-top: 80px;
    }
}

    @media only screen and (min-width: 1800px) {
        #title {
            font-size: 10rem;
            top: 40%;
        }
    }

    @media only screen and (max-width: 1000px) {
        #title {
            font-size: 4rem;
            top: 22%;
        }
    }

    @media only screen and (max-width: 575px) {
        #title {
            font-size: 2rem;
            top: 12%;
        }
    }

    /* Title resizing */

    @keyframes wave {
        0%,40%,100% {
            transform: translateY(0)
        }
        20% {
            transform: translateY(-20px)
        }
    }

    .main-interface-container {
        position: relative;
    }

    #main-interface {
        display: block;
        position: relative;
        user-select: none;
        pointer-events: none;
        filter: brightness(70%);
        z-index: 3;
        filter: grayscale(55%);
    }

    #main-interface-wave-top {
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        height: auto;
        z-index: 4;
    }

    #main-interface-wave-bottom {
        position: relative;
        z-index: 4;
        transform: rotate(180deg) translateY(4%);
        top: 0;
    }

    .shape-fill {
        fill: rgb(0, 0, 0);
        opacity: 1;
    }

    .main-container-outer {
        width: 100%;
        z-index: 4;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .main-container-inner {
        padding: 20px;
        text-align: center;
        margin: 20vh 0 20vh 0;
        transition: all ease 2s;
        width: 90%;
    }

    .main-container-outer h1 {
        margin-bottom: 10vh;
    }

    .main-container-outer p {
        margin-top: 5vh;
    }


    .main-container-outer .sponsor-list {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        flex-wrap: wrap;
        align-items: center;
        margin-bottom: 10vh;
    }

    .main-container-outer .sponsor-list .sponsor-bx {
        padding: 25px;
        transition: all ease 1s;
    }

    .main-container-outer .sponsor-list img {
        width: 150px;
        transition: all .2s ease-in-out;
    }
    @media (max-width: 700px) {
        .main-container-outer .sponsor-list img {
            width: 110px;
        }
    }

    .main-container-outer .sponsor-list img:hover {
        transform: scale(1.15);
    }

</style>
<script>
export default {
    name: "Hero"
}
</script>
<template>
    <div class = "hero">
        <img class = "hero-ill" src = "../assets/images/illustration-working.svg"/>
        <div class="hero-text">
            <h1>More than just shorter links</h1>
            <p>Build your brand's recognition and get detailed insights on how your links are performing</p>
            <button class = "rounded-btn hero-btn">Get Started</button>
        </div>
    </div>
</template>
<style>
    .hero{
        position: relative;
        text-align: center;
        overflow-x: hidden;
        display: flex;
        flex-direction: column;
        gap: 1.5em;
    }
    .hero-ill{
        width: 140%;
        margin-left: .5em;
    }
    .hero-text{
        margin: 0 1em;

    }
    h1{
        line-height: 1.2em;
        font-size: 2em;
        /* font-size: calc(1em + 0.5em + 3em); */
    }
    p{
        font-size: 1em;
        line-height: 1.4em;
        color: gray;
        padding: 1em 0;
    }
    .hero-btn{
        font-size: 1em;
    }
    @media screen and (min-width: 768px){
        .hero{
            display: grid;
            grid-template-columns: 1fr 1fr;
            align-items: center;
            grid-template-areas: "a b";
            gap: 2em;
        }
        .hero-ill{
            grid-area: b;
            width: 100%;
        }
        .hero-text{
            grid-area: a;
            margin-left: 5em;
            text-align: left;
        }
        p{
            padding: 1em 0;
            font-size: 1.5vw;
        }
        h1{
            font-size: 4.5vw;
        }
        .hero-btn{
            font-size: 1.5  vw;
        }
    }
</style>
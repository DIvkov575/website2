<script lang="ts">
    import Countup from './lib/Countup.svelte'
</script>

<main>


    <div id="d1">
        <div id="d1-inner">
            <h1>Belmont School of <span>Code<div style="background-color: white; display: inline-block; height: 0.8rem; width: 0.8rem; border-radius: 6%; margin-left: 1px;"></div></span></h1>
        </div>
    </div>

    <div id="d2">
        <div id="d2-inner">
            <a><h2>About BSC</h2></a>
            <h3>BSC is a non-profit organization, devoted to creating a computer science education, accessible to everyone.</h3>
            <h3>BSC offers seminars and classes, with proceedings going towards improving the BSC content and education charities in Boston</h3>

            <div id="counters">
                <div class="box"><h3><Countup value={18}/>+ Alumni</h3></div>
                <div class="box"><h3>$<Countup value={2000}/>+ donated</h3></div>
            </div>

        </div>
    </div>

    <div id="d3">
        <div id="d3-inner">
            <a><h2>BSC <a class="box" style="margin-left: 0.1rem">Boston</a> 2024</h2></a>
            <div style="height: 0.4rem"></div>
            <h3>2 FREE virtual seminars on <u>July 13-14, 2024</u> from <u>6:00-7:30 PM</u></h3>
            <h3> Topics include: Web design with Google Sites and Wix, internet and website architecture, building websites in HTML/CSS, and publishing website with Vercel</h3>

            <a href=""><img src="" alt=""></a>
        </div>
    </div>

    <div id="d4">
        <div id="d4-inner">
            <a><h2><a class="box">Learn</a>to code!</h2></a>
            <div style="height: 0.6rem"></div>

            <h3>Affordable Python classes for middle and high-schoolers. Proceedings go towards charity. Course completion time varies.</h3>
            <div style="height: 0.2rem"></div>

            <ul>
                <li><h3>Variables, operators, conditions, Loops, builtin Data-structures</h3></li>
                <li><h3>OOP, Decorators, Lambda, Error handling</h3></li>
                <li><h3>Students choice of Website development, Games, Data-Science or Algorithms</h3></li>
            </ul>

            <a href=""><img src="" alt=""></a>
        </div>
    </div>
    <div id="d5">
        <div id="d5-inner">
        </div>
    </div>

</main>

<style>
</style>

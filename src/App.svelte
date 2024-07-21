<script lang="ts">
    import Countup from './lib/Countup.svelte'

    let visible = true;
    const gmailClick = () => {
        setTimeout(() => {
            visible = false;
        }, 15000)
    }
</script>

<main>
<!--    https://github.com/DIvkov575/BSC2.3-->


    <div id="d1">
        <div id="d1-inner">
            <div id="logo"><img src="
            /favicon.svg" alt="logo"></div>
            <h1>Belmont School of Code.</h1>
        </div>
    </div>

    <div id="d2">
        <a class="box" style="padding: 0 0.75rem 0 0.75rem"><h2>About BSC</h2></a>
        <div style="height: 0.5rem"></div>
        <h3>BSC is a non-profit organization, devoted to creating a computer science education, accessible to everyone.</h3>
        <h3>BSC offers seminars and classes, with proceedings going towards improving the BSC content and education charities in Boston</h3>

        <div id="counters">
            <div class="box"><h3><Countup value={15}/>+ Alumni</h3></div>
            <div class="box"><h3>$<Countup value={2500}/>+ donated</h3></div>
        </div>

    </div>

    <div class="full-width-container" id="d3">
        <div class="inner-full-width-container">
            <h2>BSC <a href="https://forms.gle/Uy89J5CXqN9rJrvi9" target="_blank" class="box" style="margin-left: 0.1rem">Boston</a> 2024</h2>
            <div style="height: 0.75rem"></div>
            <h3>2 FREE virtual seminars <u>July 13&14,  2024</u> from <u>6:00-7:30 PM</u></h3>
            <h3> Topics include: Web design with Google Sites and Wix, internet and website architecture, building websites in HTML/CSS, and publishing website with Vercel</h3>
            <h3>$200 / 20 classes</h3>
        </div>


        <a href="https://forms.gle/Uy89J5CXqN9rJrvi9" target="_blank">
            <div class="Qr-Wrapper">
                <img src="/BSCBOSTONQR.png" alt="BSC-Boston-Qr-code">
                <h3>Click Me</h3>
            </div>
        </a>
    </div>

    <div class="full-width-container" id="d4">
        <div class="inner-full-width-container">
            <h2><a href="https://forms.gle/T7vFU1fbsx5aQjJs8" target="_blank" class="box">Learn</a>to code!</h2>
            <div style="height: 0.75rem"></div>

            <h3>Affordable Python classes for middle and high-schoolers. Proceedings go towards charity. Course completion time varies.</h3>
            <div style="height: 0.2rem"></div>

            <ul>
                <li><h3>Variables, operators, conditions, Loops, builtin Data-structures</h3></li>
                <li><h3>OOP, Decorators, Lambda, Error handling</h3></li>
                <li><h3>Students choice of Website development, Games, Data-Science or Algorithms</h3></li>
            </ul>
        </div>

        <a href="https://forms.gle/T7vFU1fbsx5aQjJs8" target="_blank">
            <div class="Qr-Wrapper">
                <img src="/BSCPYTHONQR.png" alt="BSC-Boston-Qr-code">
                <h3>Click Me</h3>
            </div>
        </a>
    </div>

    <div id="d5" class="full-width-container">
        <div class="inner-full-width-container">
            <h2><a href="https://account.venmo.com/u/Belmontcodes" target="_blank" class="box">Donate</a>!</h2>
            <div style="height: 0.75rem"></div>

            <h3>Your funds will go towards:</h3>
            <h3>Improving our content, making free seminars possible, site & service fees, and various charities in the Boston Area</h3>

            <div style="height: 1.4rem"></div>
            <h3>Anything Helps</h3>
        </div>

        <a href="https://account.venmo.com/u/Belmontcodes" target="_blank" >
            <div class="Qr-Wrapper">
                <img src="/VenmoQr.png" alt="BSC-Boston-Qr-code">
                <h3 style="top: -0.75rem">Click Me</h3>
            </div>
        </a>
    </div>

    <div id="footer">
        <div id="footer-inner">
            <a href="https://www.linkedin.com/company/belmont-school-of-code/?viewAsMember=true"><div class="image-wrapper"><img src="/LinkedinIcon.svg" alt="linkedin-icon"></div></a>

            {#if visible}
                <div class="image-wrapper" on:click={gmailClick}><img src="/GoogleIcon.svg" alt="Google Icon"></div>
            {:else}
                <div style="padding-top: 12px"><h3>dmi194@g.harvard.edu</h3></div>
            {/if}

            <a href="https://www.instagram.com/belmontschoolofcode/"><div class="image-wrapper"><img src="/InstagramIcon.svg" alt="instagram-icon"></div></a>
        </div>
    </div>

</main>

<style>
</style>

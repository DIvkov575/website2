<script lang="ts">
    import {fly} from 'svelte/transition';

    import { inview } from 'svelte-inview';

    import Countup from './lib/Countup.svelte';

    let visible = true;
    const gmailClick = () => {
        setTimeout(() => {
            visible = false;
        }, 15000)
    }

    let options1 =  {}
    let options2 = {}

    let show_d2 = false;
    let show_d3 = false;
    let show_d4 = false;
    let show_d5 = false;
</script>

<main>
    <button style="width: 500px" on:click={() => {show_d2 = !show_d2; show_d3 = !show_d3; show_d4 = !show_d4; show_d5 = !show_d5}}></button>

    <div id="d1">
        <img src="/bg2.png" alt="generic bg">
        <div>
            <h1>Belmont School of Code.</h1>
        </div>
    </div>

    <div
        class="fw-wrapper"
        use:inview={options1}
        on:inview_leave ={(_) => show_d2 = false}
        on:inview_enter ={(_) => show_d2 = true}>

        {#if show_d2}
            <div transition:fly={{x: -200, duration: 800}} class="fw-container" id="d2">
                <h1 style="color: black">BSC</h1>
                <div style="height: 0.5rem"></div>
                <h3>BSC is a non-profit organization, devoted to creating a computer science education, accessible to everyone.</h3>
                <h3>BSC offers seminars and classes, with proceedings going towards improving the BSC content and education charities in Boston</h3>

                <div id="counters">
                    <div class="box"><h3><Countup value={15}/>+ Alumni</h3></div>
                    <div class="box"><h3>$<Countup value={2500}/>+ donated</h3></div>
                </div>

                <div id="npo_logos">
                    <div class="logo-wrapper"><img src="/gwc_logo.png" alt="gwc_logo"></div>
                    <div class="logo-wrapper"><img src="/BEDF_logo.jpeg" alt="Boston Education Fund logo"></div>
                    <div class="logo-wrapper"><img src="/bgc_logo.png" alt="black girls who code logo"></div>
                </div>
            </div>
        {/if}
    </div>


    <div
        class="fw-wrapper"
        use:inview={options1}
        on:inview_leave ={(_) => show_d3 = false}
        on:inview_enter ={(_) => show_d3 = true}>

        {#if show_d3}
            <div transition:fly={{x:-200, duration: 800}} class="fw-container" id="d3">
                <div class="inner-full-width-container">
                    <h1>BSC <a href="https://forms.gle/Uy89J5CXqN9rJrvi9" target="_blank" class="box" style="margin-left: 0.1rem">Boston</a> 2024</h1>
                    <div style="height: 0.75rem"></div>

                    <h3>2 FREE virtual seminars <u>July 13&14,  2024</u> from <u>6:00-7:30 PM</u></h3>
                    <h3> Topics include: Web design with Google Sites and Wix, internet and website architecture, building websites in HTML/CSS, and publishing website with Vercel</h3>
                </div>

                <a href="https://forms.gle/Uy89J5CXqN9rJrvi9" target="_blank">
                    <div class="Qr-Wrapper">
                        <img src="/BSCBOSTONQR.png" alt="BSC-Boston-Qr-code">
                        <h3>Click Me</h3>
                    </div>
                </a>
            </div>
        {/if}
    </div>

    <div
        class="fw-wrapper"
        use:inview={options1}
        on:inview_leave ={(_) => show_d4 = false}
        on:inview_enter ={(_) => show_d4 = true}>
        {#if show_d4}
            <div transition:fly={{x:-200, duration: 800}} class="fw-container" id="d4">
                <div class="inner-full-width-container">
                    <h1><a href="https://forms.gle/T7vFU1fbsx5aQjJs8" target="_blank" class="box">Learn</a>to code</h1>
                    <div style="height: 0.75rem"></div>
                    <h3>Affordable Python classes for middle and high-schoolers. Proceedings go towards charity</h3>
                    <ul style="margin: 0.5rem auto 0.75rem auto; padding-left: 1.5rem">
                        <li><h3>Fundamentals: operators, conditions, Loops, etc</h3></li>
                        <li><h3>Student Choice: Web development, Games, or Data-Science</h3></li>
                    </ul>
                    <h3>$200 / 20 classes</h3>
                </div>

                <a href="https://forms.gle/T7vFU1fbsx5aQjJs8" target="_blank">
                    <div class="Qr-Wrapper">
                        <img src="/BSCPYTHONQR.png" alt="BSC-Boston-Qr-code">
                        <h3>Click Me</h3>
                    </div>
                </a>
            </div>
        {/if}
    </div>

    <div
        class="fw-wrapper"
        use:inview={options1}
        on:inview_leave ={(_) => show_d5 = false}
        on:inview_enter ={(_) => show_d5 = true}>
        {#if show_d5}
            <div transition:fly={{x:-200, duration: 800}} id="d5" class="fw-container">
                <div class="inner-full-width-container">
                    <h1><a href="https://account.venmo.com/u/Belmontcodes" target="_blank" class="box">Donate</a> Now</h1>
                    <div style="height: 0.75rem"></div>

                    <h3>Your funds will go towards:</h3>
                    <h3>Improving our content, making free seminars possible, site & service fees, and various charities in the Boston Area</h3>

                </div>

                <a href="https://account.venmo.com/u/Belmontcodes" target="_blank" >
                    <div class="Qr-Wrapper">
                        <img src="/VenmoQr.png" alt="BSC-Boston-Qr-code">
                        <h3 style="top: -0.75rem">Click Me</h3>
                    </div>
                </a>
            </div>
        {/if}
    </div>

    <div id="footer">
        <div id="footer-inner">
            <a href="https://www.linkedin.com/company/belmont-school-of-code/?viewAsMember=true"><div class="image-wrapper"><img src="/LinkedinIcon.svg" alt="linkedin-icon"></div></a>

            {#if visible}
                <button class="image-wrapper" on:click={gmailClick} ><img src="/GoogleIcon.svg" alt="Google Icon"></button>
            {:else}
                <div style="padding-top: 12px"><h3>dmi194@g.harvard.edu</h3></div>
            {/if}

            <a href="https://www.instagram.com/belmontschoolofcode/"><div class="image-wrapper"><img src="/InstagramIcon.svg" alt="instagram-icon"></div></a>
        </div>
    </div>

</main>

<style>
</style>

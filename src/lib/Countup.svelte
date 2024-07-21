<script>
    import {nanoid} from "nanoid";
    import {inview} from "svelte-inview";

    const id = nanoid();

    let isInView;

    export let value = 0;
    export let duration = 1000;
    export let step = 1;

    const counterResult = [];
    const timers = [];

    const max = parseInt(value);
    while (duration / ((max - 0) / step) < 2) step++;
    counterResult[id] = 0;
    timers[id] = setInterval(
        () => {
            if (isInView) {
                if (counterResult[id] < max) {
                    counterResult[id] += step;
                } else {
                    clearInterval(timers[id]);
                    counterResult[id] = max
                }
            }
        },
        duration / (max / step)
    );
</script>

<span use:inview on:change={(event) => {
    const { inView } = event.detail;
    isInView = inView;
  }}>
    {counterResult[id].toLocaleString()}
</span>
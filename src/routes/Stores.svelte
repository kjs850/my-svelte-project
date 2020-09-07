<script>
    import { count } from './stores/store.js';
    import Incrementer from './stores/Incrementer.svelte';
    import Decrementer from './stores/Decrementer.svelte';
    import Resetter from './stores/Resetter.svelte';

    let count_value;

    const unsubscribe = count.subscribe(value => {
        count_value = value;
    });
</script>

<h1>The count is {count_value}</h1>

<Incrementer/>
<Decrementer/>
<Resetter/>
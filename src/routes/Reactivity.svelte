<script>
    let count = 1;

    // the `$:` means 're-run whenever these values change'
    $: doubled = count * 2;
    $: quadrupled = doubled * 2;

    function handleClick() {
        count += 1;
    }

    $: if (count >= 10) {
        alert(`count is dangerously high!`);
        count = 9;
    }

</script>

<div id="#jb-content">
    <button on:click={handleClick}>
        Count: {count}
    </button>

    <p>{count} * 2 = {doubled}</p>
    <p>{doubled} * 2 = {quadrupled}</p>
</div>
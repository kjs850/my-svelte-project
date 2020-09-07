<script>
    let user = { loggedIn: false };

    function toggle() {
        user.loggedIn = !user.loggedIn;
    }
    ////
    let cats = [
        { id: 'J---aiyznGQ', name: 'Keyboard Cat' },
        { id: 'z_AbfPXTKms', name: 'Maru' },
        { id: 'OUtn3pvWmpg', name: 'Henri The Existential Cat' }
    ];

    ////
    let promise = getRandomNumber();

    async function getRandomNumber() {
        const res = await fetch(`https://svelte.dev/tutorial/random-number`);
        const text = await res.text();

        if (res.ok) {
            return text;
        } else {
            throw new Error(text);
        }
    }

    function handleClick() {
        promise = getRandomNumber();
    }

</script>

<div id="#jb-content">
    <h2>if...else...</h2>
    {#if user.loggedIn}
        <button on:click={toggle}>
            Log out
        </button>
    {:else}
        <button on:click={toggle}>
            Log in
        </button>
    {/if}

    <h2>each...</h2>

    <ul>
        {#each cats as { id, name }, i}
            <li><a target="_blank" href="https://www.youtube.com/watch?v={id}">
                {i + 1}: {name}
            </a></li>
        {/each}
    </ul>


    <h2>Await Blocks</h2>
    <button on:click={handleClick}>
        generate random number
    </button>

    {#await promise}
        <p>...waiting</p>
    {:then number}
        <p>The number is {number}</p>
    {:catch error}
        <p style="color: red">{error.message}</p>
    {/await}

</div>
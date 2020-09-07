<script>
    import Nested from './props/Nested.svelte';
    import Info from './props/Info.svelte';

    const pkg = {
        name: 'svelte',
        version: 3,
        speed: 'blazing',
        website: 'https://svelte.dev'
    };


</script>

<div id="#jb-content">
    <Nested answer={42}/>
    <h2>Default Values</h2>
    <Nested/>
    <h2>Spread Props</h2>
    <Info {...pkg}/>
</div>

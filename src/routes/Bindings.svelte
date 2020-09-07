<script>
    let name = '';

    let a = 1;
    let b = 2;

    let w;
    let h;
    let size = 42;
    let text = 'edit me';
</script>

<h2>Text inputs</h2>

<input bind:value={name} placeholder="enter your name">
<p>Hello {name || 'stranger'}!</p>

<h2>numeric inputs</h2>

<label>
    <input type=number bind:value={a} min=0 max=10>
    <input type=range bind:value={a} min=0 max=10>
</label>

<label>
    <input type=number bind:value={b} min=0 max=10>
    <input type=range bind:value={b} min=0 max=10>
</label>

<p>{a} + {b} = {a + b}</p>

<h2>dimensions</h2>
<input type=range bind:value={size}>
<input bind:value={text}>

<p>size: {w}px x {h}px</p>

<div bind:clientWidth={w} bind:clientHeight={h}>
    <span style="font-size: {size}px">{text}</span>
</div>

<style>
    input { display: block; }
    div { display: inline-block; }
</style>
<script>
    let src = 'https://svelte.dev//tutorial/image.gif';
    let name = 'Rick Astley';

    let string = `here's some <strong>HTML!!!</strong>`;

</script>

<div id="#jb-content">
    <!--    이미지넣기  -->
    <img {src} alt="{name} dancing">

    <!--    스타일-->
    <p id="p">Styled!</p>

    <!--    html tag-->
    <p>{@html string}</p>

</div>

<style>
    p {
        color: purple;
        font-family: 'Comic Sans MS', cursive;
        font-size: 2em;
    }
</style>
<script>
    import Inner from './events/Inner.svelte';

    function handleMessage(event) {
        alert(event.detail.text);
    }
</script>
<!--https://beomy.github.io/tech/svelte/events/-->
<Inner on:message={handleMessage}/>
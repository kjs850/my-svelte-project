<script>
    import Navi from "./routes/Navi.svelte";
	export let name;

</script>

    <body>
        <div id="jb-container">
            <div id="jb-header">
                Hello {name}!
            </div>

            <Navi/>

        </div>
    </body>

<style>

    #jb-container {
        width: 940px;
        margin: 0px auto;
        padding: 20px;
        border: 0px solid #bcbcbc;
    }
    #jb-header {
        padding: 20px;
        margin-bottom: 20px;
        border: 1px solid #bcbcbc;
    }
    #jb-footer {
        clear: both;
        padding: 20px;
        border: 1px solid #bcbcbc;
    }
</style>
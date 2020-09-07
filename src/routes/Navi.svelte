<script>
    import Router from 'svelte-spa-router'

    import Home from './Home.svelte'
    import Intro from './Intro.svelte'
    import Reactivity from './Reactivity.svelte'
    import Props from './Props.svelte'
    import Logic from './Logic.svelte'
    import Events from './Events.svelte'
    import Bindings from './Bindings.svelte'
    import LifeCycle from './LifeCycle.svelte'
    import Stores from './Stores.svelte'


    import NotFound from './NotFound.svelte'

    export const routes = {
        // Exact path
        '/': Home,
        '/intro': Intro,
        '/reactivity': Reactivity,
        '/props': Props,
        '/logic': Logic,
        '/events': Events,
        '/bindings': Bindings,
        '/lifeCycle': LifeCycle,
        '/stores': Stores,



        // Using named parameters, with last being optional
        //'/author/:first/:last?': Author,

        // Wildcard parameter
        //'/book/*': Book,

        // Catch-all
        // This is optional, but if present it must be the last
        '*': NotFound,
    }
</script>

<div id="jb-sidebar">
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/#/intro">Intro</a></li>
        <li><a href="/#/reactivity">Reactivity</a></li>
        <li><a href="/#/props">Props</a></li>
        <li><a href="/#/logic">Logic</a></li>
        <li><a href="/#/events">Events</a></li>
        <li><a href="/#/bindings">Bindings</a></li>
        <li><a href="/#/lifeCycle">LifeCycle</a></li>
        <li><a href="/#/stores">Stores</a></li>

        <li><a href="/#/notFound">NotFound</a></li>
    </ul>
</div>
<div id="jb-content">
    <Router {routes}/>
</div>


<style>
    #jb-content {
        width: 580px;
        padding: 20px;
        margin-bottom: 20px;
        float: left;
        border: 1px solid #bcbcbc;
    }
    #jb-sidebar {
        width: 260px;
        padding: 20px;
        margin-bottom: 20px;
        float: right;
        border: 1px solid #bcbcbc;
    }
</style>

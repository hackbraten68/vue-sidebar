<template>
    <main>
        <div class="desktop-wrapper">
            <div class="container">
                <div class="nav-bar">
                    <div class="widget-navbar">
                        <Navbar />
                    </div>
                </div>

                <div class="left-col">
                    <div class="widget-card">
                        <ToDo />
                    </div>
                </div>
                <div class="center-col">
                    <div class="widget-card">

                    </div>
                </div>
                <div class="top-right-col">
                    <div class="widget-card small-card">

                    </div>
                </div>
                <div class="bottom-right-col">
                    <div class="widget-card small-card">

                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<script setup>
import Navbar from '../components/Navbar.vue'
import ToDo from '../components/ToDo.vue';

</script>

<style lang="scss" scoped>
    main {
        background-color: var(--dark-alt);
    }
    .container {  
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 0.3fr 1.3fr 1.4fr;
        gap: 0.5em 0.5em;            
        grid-auto-flow: row;
        grid-template-areas:
            "nav-bar nav-bar nav-bar"
            "left-col center-col top-right-col"
            "left-col center-col bottom-right-col";
    }

    .nav-bar {
        grid-area: nav-bar;
    }
    .left-col {
        grid-area: left-col;
    }
    .center-col {
        grid-area: center-col;
    }
    .top-right-col {
        grid-area: top-right-col;
    }
    .bottom-right-col {
        grid-area: bottom-right-col;
    }
    .widget-card, widget-navbar {
        width: 100%;
        height: 75vh;

        background-color: var(--light);
        box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
        border: none;
        border-radius: 0.625em;

        padding: 2em;
    }

    .widget-navbar {
        height: 3em;
        background-color: var(--light);

        box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
        border: none;
        border-radius: 0.625em;

        margin-bottom: 4em;
    }

    .small-card {
        height: 100%;
    }
</style>
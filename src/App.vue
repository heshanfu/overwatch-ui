<template>
    <div id="app">
        <div class="present">
            <ow-button @click="isOpen = true">Open</ow-button>
            <ow-modal :is-open="isOpen">
                <div style="display: flex; flex-direction: column; align-items: center;">
                    <p style="font-size: 3em">ADD A NEW FRIEND</p>
                    <p style="margin: 12px">INPUT A GAME ID OR EMAIL ADDRESS</p>
                    <ow-input placeholder="Game ID or Email Address" :width="300"></ow-input>
                </div>
                <template slot="footer">
                    <ow-button>BACK</ow-button>
                    <ow-button type="warning">SEND REQUEST</ow-button>
                </template>
            </ow-modal>
        </div>
        <past></past>
    </div>
</template>

<script>
    import Past from './Past'

    export default {
        name: 'app',
        data() {
            return {
                isOpen: true
            }
        },
        methods: {
        },
        components: { Past },
        mounted() {
        }
    }
</script>

<style lang="scss">
    * {
        font-family: -apple-system,BlinkMacSystemFont,Segoe UI,Helvetica,Arial,sans-serif,Apple Color Emoji,Segoe UI Emoji,Segoe UI Symbol;
    }
    #app {
        position: relative;
        padding: 100px 100px;
        background: url("./assets/images/bg.png");
        .present {
            margin-bottom: 100vh;
        }
        .badge-item {
            margin: 0 20px;
        }
    }
</style>
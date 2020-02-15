<template>
    <div class="container">
        <div class="row">
            <my-header></my-header>
        </div>
        <hr>
        <div class="row">
            <my-servers></my-servers>
          <!--    status-->
            <my-status></my-status>
        </div>
        <hr>
        <div class="row">
        <!--   footer-->
            <my-footer></my-footer>
        </div>
    </div>
</template>

<script>
    import Header from "./components/Header.vue";
    import Status from "./components/Status.vue";
    import Servers from "./components/Servers.vue";
    import Footer from "./components/Footer.vue";
    export default {

        components:{
            'my-header': Header,
            'my-servers': Servers,
            'my-status': Status,
            'my-footer': Footer
        }
    }
</script>

<style>

</style>

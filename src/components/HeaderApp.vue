<script>
export default {
    name: 'HeaderApp',
    data() {

    }
}
</script>

<template>
    <div class="container ">
        <div class="row justify-between align-center ">
            <div class="navigatore col d-flex">
                <div>Donna</div>
                <div>Uomo</div>
                <div>Bambino</div>
            </div>

            <div class="col d-flex align-center">
                <img class="logo" src="../assets/img/boolean-logo.png" alt="">
            </div>
            <div class="col utente">
                <img src="" alt="profilo">
                <img src="" alt="likes">
                <img src="" alt="carrello">
            </div>
        </div>
    </div>
</template>

<style>
header {
    background-color: orange;
    width: 100%;
    position: fixed;
    height: 40px;
    z-index: 1;

    .container {
        margin-top: 9px;
        color: white;
    }
}
</style>
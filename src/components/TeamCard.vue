<template>
    <div id="grupo145" class="card text-white bg-dark " style="height: 600px;">
                <div class="d-flex justify-content-center p-2">
                    <img :src="member.imagen" alt="fotografia miembro" width="250">

                </div>
                <div class="card-body">
                    <h3 class="card-title text-center">{{ member.nombre }}</h3>
                    <p class="card-text">{{ member.descripcion }}</p>
                    <p class="card-text"> <span>Rol: </span> {{ member.rol }}</p>
                    <p class="card-text"> <span>Codigo: </span> {{ member.codigo }}</p>
                </div>
                

     </div>

</template>

<script>
    export default {
        name: "TeamCard",
        props: ['member']
    }
</script>

<style scoped>

</style>

<template>
    <div class="card bg-dark">
      <div class="card bg-light" id="team" >
            <span  class="d-flex-justify-content-center p-2" >
                    <img class="mx-auto d-block border border-info" :src= "member.imagen" style="mg-style" alt="Miembros del equipo"/>
                    <div class="card-body">
                    <h5 class="card-title">{{ member.nombre }}</h5>
                    <p class="card-text " >
                    <p class="text-justify">    
                        {{ member.descripcion }}
                    </p>
                    <p class="card-text font-italic"><small>Rol: {{ member.rol }}</small></p>
                    </div>
            </span>
        </div>   
    </div>
</template>

<script>
    export default {
        name: "TeamCard",
        props: {
            member: {
                type: Object,
                required: true,
            }

        }
    }

</script>

<style scoped>

</style>

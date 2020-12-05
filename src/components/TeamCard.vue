<template>
    <div class="card bg-dark">
      <div class="card bg-light" id="team" >
            <span  class="d-flex-justify-content-center p-2" >
                    <img class="mx-auto d-block border border-info" :src= "imagen" style="mg-style" alt="Miembros del equipo"/>
                    <div class="card-body">
                    <h5 class="card-title">{{nombre}}</h5>
                    <p class="card-text " >
                    <p class="text-justify">    
                        {{descripcion}}
                    </p>
                    <p class="card-text font-italic"><small>Rol: {{rol}}</small></p>
                    </div>
            </span>
        </div>   
    </div>
</template>

<script>
    export default {
        name: "TeamCard",
        props: {
            codigo: {
                type: Number,
                required: true,

            },
            nombre: {
                type: String,
                required: true,

            },
            descripcion: {
                type: String,
                required: true,

            },
            rol: {
                type: String,
                required: true,

            },
             imagen: {
                type: String,
                required: true,

            }

        }
    }

</script>

<style lang="css" scoped>

</style>

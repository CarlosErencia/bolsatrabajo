<template>
    <div class="border">
        <h2>{{infoOferta.titulo}}</h2>
        <p>{{infoOferta.descripcion}}</p>
        <b-button variant="success" @click="inscrito">{{infoOferta.inscrito}}</b-button>
        <hr/>
    </div>
</template>

<script>
export default {
    name: 'Oferta',
    data: function(){
        return{

        }
    },
    props: {
        infoOferta: {}
    },
    methods: {
        like: function(){
            console.log("Se ha sumado un like! " + this.infoExperiencia.id)
            this.infoExperiencia.likes ++;
            this.axios.put('http://labs.iam.cat/~a17jorcermar/M06/viajesvue/Backend/api.php/records/EXPERIENCIA/' + this.infoExperiencia.id, {likes: this.infoExperiencia.likes}).then(() => {})
            },
            
        }
    }

</script>
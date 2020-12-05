<template>
  <div id="App">
    <NavBar />
    <div class="card-group" >
      <TeamCard 
      class="col-md-3" 
      v-for="integrante in this.integrantes" 
      :key="integrante.key" 
      :codigo="integrante.codigo" 
      :nombre="integrante.nombre" 
      :descripcion="integrante.descripcion"
      :rol="integrante.rol"
      :imagen="integrante.imagen"/>
    </div>
  </div>
</template>

<script>
import NavBar from './components/NavBar';
import TeamCard from './components/TeamCard';
export default {
  name: 'App',
  data() {
    return {
      integrantes: [
        {
        codigo: 1,
        nombre: "Juan Camilo Fonseca",
        descripcion:
          "Mi nombre es Juan Camilo Fonseca Gomez , Nací en Bogotá el 4 de julio del 2002, me gradué de bachiller en el 2019 del colegio claretiano de Bosa y en este momento estoy cursando el 3 trimestre en el tecnologo de mecatronica en el servicio nacional de aprendizaje SENA , y estoy en el curso de Misión TIC 2022",
        rol:"Desarrollador Backend",
        imagen:"https://res.cloudinary.com/dkgxa2bjf/image/upload/c_scale,w_250/v1607144096/WhatsApp_Image_2020-11-28_at_11.28.54_PM_1_x18gvw.jpg",
        },
        {
        nombre: "Viviana Marcela Chacón",
        descripcion:
          "Soy Viviana Marcela Chacón, tengo 35 años, soy de la  de Bucaramanga pero por temas laborales resido en la ciudad de Bogotá, soy ingeniera devops, por 5 años trabajé como ingeniera de pruebas de calidad de software. Me encanta bailar, escuchar música y leer, este año decidí pertenecer a Misión TIC 2022.",
        rol:"Desarrolladora Frontend",
        imagen:"https://res.cloudinary.com/dkgxa2bjf/image/upload/c_scale,w_250/v1607137239/vivi_uo0iip.jpg",
         },
        {
        codigo: 3,
        nombre: "Carlos Esteban Escudero",
        descripcion:
          "Joven de 21 años, nacido en Sincelejo, Sucre el 21 de marzo de 1999. En 2015 se graduó con honores de bachiller, en la Institución Educativa Normal Superior de Sincelejo. Actualmente es estudiante de último semestre de Ingeniería de Sistemas de la Corporación Universitaria del Caribe CECAR, esta vinculado a Misión TIC 2022.",
        rol:"Arquitecto",
         imagen:"https://res.cloudinary.com/dkgxa2bjf/image/upload/c_scale,h_250,w_250/v1607144629/Captura_de_Pantalla_2020-12-05_a_la_s_12.03.07_a._m._oyatic.png",
        },
        {
        codigo: 4,
        nombre: "Robinson",
        descripcion:
          "Soy Robinson Martínez, tengo 33 años, Ingeniero electrónico especialista en Aplicación de tecnologías digitales a la educación de la universidad de Santander, docente de tecnología e informática en Medellín. Nací en Palmira, graduado del instituto técnico industrial Humberto Raffo Rivera, y pertenezco a Misión TIC 2022.",
        rol:"Scrum Master",
         imagen:"https://res.cloudinary.com/dkgxa2bjf/image/upload/c_scale,h_250,w_250/v1607144107/WhatsApp_Image_2020-11-28_at_4.39.25_PM_yt7tme.jpg",
        }
      ]
    }
  },
  components: {
    TeamCard,
    NavBar,
  }
}
</script>


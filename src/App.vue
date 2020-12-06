<template>
  <div id="app" class="bg-dark" >
  <div class="container-fluid">
    <NavBar />
    <Carousel />
    <div class="container-fluid">
      <Divider title="Servicios" />
      <Services />
      <Divider title="Noticias" />
      <div id="news" class="row row-cols-1 row-cols-md-2">
        <NewsCard
          v-for="(notice, index) in this.news.slice(0, 4)"
          :key="index"
          :author="notice.author"
          :title="notice.title"
          :description="notice.description"
          :url="notice.url"
          :image="notice.urlToImage"
          :date="notice.publishedAt"
        />
      </div>
    </div>
    <Divider title="Equipo" />
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
      <Divider title="Footer" />
      <FooterPag id="footer"/>
    </div>
  </div>
</template>

<script>
import NavBar from "./components/NavBar";
import Carousel from "./components/Carousel";
import Services from './components/Services'
import NewsCard from "./components/NewsCard";
import Divider from "./components/Divider";
import TeamCard from "./components/TeamCard";
import FooterPag from "./components/FooterPag";
import axios from "axios";
export default {
  name: "App",
  data() {
    return {
      news: [],
      integrantes: [
        {
          codigo: 1,
          nombre: "Juan Camilo Fonseca",
          descripcion:
            "Mi nombre es Juan Camilo Fonseca Gomez , Nací en Bogotá el 4 de julio del 2002, me gradué de bachiller en el 2019 del colegio claretiano de Bosa y en este momento estoy cursando el 3 trimestre en el tecnologo de mecatronica en el servicio nacional de aprendizaje SENA , y estoy en el curso de Misión TIC 2022",
          rol: "Desarrollador Backend",
          imagen:
            "https://res.cloudinary.com/dkgxa2bjf/image/upload/c_scale,w_220/v1607144096/WhatsApp_Image_2020-11-28_at_11.28.54_PM_1_x18gvw.jpg",
        },
        {
          codigo: 2,
          nombre: "Viviana Chacón",
          descripcion:
            "Soy Viviana Marcela Chacón, tengo 35 años, soy de Bucaramanga pero por temas laborales resido en la ciudad de Bogotá, soy ingeniera devops, por 5 años trabajé como ingeniera de pruebas de calidad de software. Me encanta bailar, escuchar música y leer, este año decidí pertenecer a Misión TIC 2022.",
          rol: "Desarrolladora Frontend",
          imagen:
            "https://res.cloudinary.com/dkgxa2bjf/image/upload/c_scale,w_220/v1607137239/vivi_uo0iip.jpg",
        },
        {
          codigo: 3,
          nombre: "Carlos Escudero",
          descripcion:
            "Joven de 21 años, nacido en Sincelejo, Sucre el 21 de marzo de 1999. En 2015 se graduó con honores de bachiller, en la Institución Educativa Normal Superior de Sincelejo. Actualmente es estudiante de último semestre de Ingeniería de Sistemas de la Corporación Universitaria del Caribe CECAR, esta vinculado a Misión TIC 2022.",
          rol: "Arquitecto",
          imagen:
            "https://res.cloudinary.com/dkgxa2bjf/image/upload/c_scale,h_220,w_220/v1607144629/Captura_de_Pantalla_2020-12-05_a_la_s_12.03.07_a._m._oyatic.png",
        },
        {
        codigo: 4,
        nombre: "Robinson",
        descripcion:
          "Soy Robinson Martínez, tengo 33 años, Ingeniero electrónico especialista en Aplicación de tecnologías digitales a la educación de la universidad de Santander, docente de tecnología e informática en Medellín. Nací en Palmira, graduado del instituto técnico industrial Humberto Raffo Rivera, y pertenezco a Misión TIC 2022.",
        rol:"Scrum Master",
         imagen:"https://res.cloudinary.com/dkgxa2bjf/image/upload/c_scale,h_220,w_220/v1607144107/WhatsApp_Image_2020-11-28_at_4.39.25_PM_yt7tme.jpg",
        }
      ]
    }
  },
  components: {
    NavBar,
    Carousel,
    NewsCard,
    TeamCard,
    FooterPag,
    Divider,
    Services
  },
  methods: {
    async getNews() {
      const res = await axios.get(
        "http://newsapi.org/v2/top-headlines?country=co&category=technology&apiKey=2ab63997a09846ffa5bc1f3f43455b70"
      );
      this.news = res.data.articles.slice(0, 4);
    },
  },
  mounted() {
    this.getNews();
  },
};

</script>

<style>
#app {
  width: 1200px;
  margin-left: 10%;
}

</style>

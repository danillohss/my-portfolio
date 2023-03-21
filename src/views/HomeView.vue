<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-grey">Olá,</h1>
              <h1 class="text-white">Meu nome é Danillo</h1>
              <span class="text-grey">Sou desenvolvedor FrontEnd</span><br />
              <v-btn tile dark class="text-yellow mt-8" variant="outlined" href="profile.pdf" download>
                DOWNLOAD CURRÍCULO
              </v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <div class="div-col2">
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999" class="mt-16">
              <v-img src="photo.png" contain max-height="300"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="5">
              <div class="eggAbout">
                <v-img src="aboutMe.png" max-height="300"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h1 class="mt-16">Sobre mim</h1><br />
              <div style="width: 120px">
              </div>
              <h4 class="mt-n4">Desenvolvedor FrontEnd</h4>
              <p class="text-grey">
                Meu nome é Danillo, tenho 25 anos, trabalhei como Desenvolvedor Jr FrontEnd na empresa Comeia, localizada
                em Caruaru-PE, atualmente estou em busca de novas oportunidades e desafios. Sou um amante da tecnologia e
                apaixonado pelo desenvolvimento FrontEnd, um Dev Junior em constante aprendizado e evolução, atualmente
                estudando Vue.js, JavaScript, HTML e CSS, cada vez mais aprimorando meus conhecimentos com o passar do
                tempo. Também com total interesse de aprender novas tecnologias como Node.js por exemplo assim me tornando
                fullstack JavaScript.
              </p>
              <br />
              <!-- <p class="text-grey">
                Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Aspernatur, ullam perspiciatis fugiat temporibus laboriosam
                accusamus tempora repellendus sequi sed cum dolorum vero est.
                Placeat dicta architecto reiciendis est veniam. Unde.
              </p> -->
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" class="padd" id="projects">

      </v-col>
      <v-col cols="12" class="mt-16" id="future">
        <div>
          <v-row>
            <v-col cols="12" sm="1">
              <div class="eggFuture">
                <v-img src="future.png" max-height="250"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h1 class="mt-16">O Que esperar para o futuro?</h1><br />
              <div style="width: 120px">
              </div>
              <p class="text-grey">
                Sou uma pessoa que sempre estou pensando no futuro, seja ele pessoal ou profissional, porém hoje minhas
                realizações pessoais estão diretamente ligadas aos meus objetivos
                profissionais. O que quero para o meu futuro é me tornar um desenvolvedor JavaScript fullstack, tendo como
                principais tecnologias Node.js e Vue.js. Hoje meus estudos estão sendo focados no HTML5, CSS3, JavaScript
                e o próprio Vue.js, framework ao qual foi desenvolvido esse portfolio que você está lendo nesse momento.
                Também venho desenvolvendo meu conhecimento em outras tecnologias como Bootstrap e JQuery. Ou seja, um
                desenvolvedor Jr em constante aprendizado.
              </p>
              <br />
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="15">
            <h1 style="display: flex;
                                              justify-content: center;
                                              align-items: center;">Meus contatos
            </h1>
            <div class="contact">
              <div class="child">
                <v-btn icon="fa-brands fa-whatsapp" color="" class="mt-7" variant="outlined"></v-btn><br />
                <span class="text-caption">(81)9 9361-8055</span> <br />

                <v-btn icon="fas fa-envelope" color="" class="mt-7" variant="outlined"></v-btn><br />
                <span class="text-caption">danillohss@gmail.com </span> <br />

              </div>
              <div class="child">
                <v-btn icon="fa-brands fa-linkedin" color="" class="mt-7" variant="outlined"
                  href="https://www.linkedin.com/in/danillohss/" target="_blank"></v-btn><br />
                <span class="text-caption">@danillohss</span> <br />

                <v-btn icon="fa-brands fa-github" color="" class="mt-7" variant="outlined"
                  href="https://github.com/danillohss" target="_blank"></v-btn><br />
                <span class="text-caption">@danillohss</span> <br />
              </div>
            </div>
          </v-col>
        </v-row>
      </v-col>
    </v-container>
    <FooterView />
    <v-btn tile dark class="text-yellow mt-8" variant="outlined" @click="topPage()" id="buttonTop">TOPO
    </v-btn>
  </v-app>
</template>

<script>
import { defineComponent } from "vue";
import NavBar from "../components/NavBar.vue";
import FooterView from "../components/FooterView.vue";

export default defineComponent({
  name: "HomeView",
  components: {
    NavBar,
    FooterView
  },
  methods: {
    topPage() {
      window.scrollTo(0, 0);
    }
  }
});
</script>
<style scoped>
.v-container {
  padding: 16px 0 16px 0;
}

.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}

.head:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 5deg);
}

.head:after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -5deg);
}

.eggAbout {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #fbdf7e;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}

.eggFuture {
  display: block;
  margin-left: 1400px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #c2a7e6;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}

.first {
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}

.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}

.imgHover {
  padding: 0 200px;
}

.pre {
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}

.div-col2 {
  position: absolute;
  z-index: 9999;
  bottom: 0;
  margin-left: auto;
  margin-right: auto;
  left: 0;
  right: 0;
  text-align: center;
}

#buttonTop {
  background-color: black;
  border-radius: 60%;
  position: fixed;
  bottom: 50px;
  right: 50px;
}

.hire {
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #e9e9e9;
  margin-top: -24px;
}

.contact {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
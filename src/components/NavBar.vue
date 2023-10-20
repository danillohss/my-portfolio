<template>
    <v-app-bar app color="black" dark flat class="px-12">
        <v-spacer/>
        <v-btn text @click="scroll('about')" class="text-yellow">SOBRE MIM</v-btn>
        <v-btn text @click="scroll('skills')" class="text-yellow">Skills</v-btn>
        <v-btn text @click="scroll('projects')" class="text-yellow">Meus projetos</v-btn>
        <v-btn text @click="scroll('future')" class="text-yellow">Para o futuro</v-btn>
        <v-btn text @click="scroll('contact')" class="text-yellow">Contato</v-btn>
    </v-app-bar>
</template>

<script>
export default {
    methods: {
        scroll(refName) {
            const element = document.getElementById(refName);
            element.scrollIntoView({ behavior: "smooth" })
        }
    }
}
</script>

<style scoped>
/* Estilos padrão */
.v-btn.text-yellow {
  color: yellow;
}

/* Estilos para telas menores */
@media (max-width: 768px) {
  .v-btn.text-yellow {
    font-size: 14px; /* Tamanho de fonte menor */
    padding: 6px 12px; /* Espaçamento interno menor */
  }
}
</style>
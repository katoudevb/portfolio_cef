<template>
  <main>
    <h1>Katiana BRICOTTEAUX</h1>

    <section id="presentation">
      <h2>Présentation</h2>
      <p>Bienvenue sur mon portfolio, je suis passionné par le développement web. Je suis débutante avec une grande motivation pour ce métier.
        Avec mon expérience récente, j'acquiers de bonnes bases solides dans les langages du HTML, CSS et JavaScript.
        J'ai déjà réalisé plusieurs projets qui permettent de montrer mes compétences acquises.
        Vous trouverez dans ce portfolio quelques exemples ainsi que des illustrations de mes réalisations.
      </p>
    </section>

    <section id="projet">
      <h2>Mes projets</h2>
      <p>Venez découvrir mes capacités techniques :</p>
      <button class="card" @click="showModal1 = true">Ouvrir CV HTML</button>
      <button class="card" @click="showModal2 = true">Ouvrir Cahier des charges</button>
      <button class="card" @click="showModal3 = true">Ouvrir Dynamiser un commentaire</button>
    </section>

    <!-- Modale 1 (CV) -->
    <Modal :isOpen="showModal1" @close="showModal1 = false">
      <h2>CV HTML</h2>
      <img :src="cvImage" alt="CV Image" class="modal-image">
      <p>Utilisation des langages HTML et CSS</p>
      <a href="https://github.com/katoudevb/Cv_CEF" target="_blank">Télécharger mon CV</a>
      <p class="creation-date">Date de création : {{ creationDate1 }}</p> 
    </Modal>

    <!-- Modale 2 (Cahier des charges) -->
    <Modal :isOpen="showModal2" @close="showModal2 = false">
      <h2>Cahier des charges</h2>
      <img :src="cahierDesChargesImage" alt="Cahier des charges" class="modal-image">
      <p>Utilisation d'aucun langages mais d'un cahier des charges</p>
      <a href="../pdf/CDC devoir.pdf" target="_blank">Télécharger mon Cahier des Charges</a>
      <p class="creation-date">Date de création : {{ creationDate2 }}</p>
    </Modal>

    <!-- Modale 3 (Commentaires) -->
    <Modal :isOpen="showModal3" @close="showModal3 = false">
      <h2>Commentaire</h2>
      <img :src="commentaireImage" alt="Commentaire Image" class="modal-image">
      <p>Utilisation du langages HTML et JavaScript</p>
      <a href="https://github.com/katoudevb/Dynamiser_commentaire" target="_blank">Télécharger mon Commentaire Dynamique</a>
      <p class="creation-date">Date de création : {{ creationDate3 }}</p>
    </Modal>
  </main>
</template>

<script setup>
import { ref } from 'vue';
import Modal from '@/components/Modal.vue';

// Déclaration des images
import cvImage from '@/assets/img/capture_cv.png'
import cahierDesChargesImage from '@/assets/img/Cdc.png'
import commentaireImage from '@/assets/img/Commentaire.png'


const showModal1 = ref(false); 
const showModal2 = ref(false); 
const showModal3 = ref(false); 

const creationDate1 = '01 Novembre 2024'; 
const creationDate2 = '05 Janvier 2025'; 
const creationDate3 = '05 Février 2025'; 
</script>

<style scoped>
h1 {
  margin-top: 3rem;
}

h2 {
  text-align: left;
  margin-top: 1rem;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif
}

.modal-image {
  width: 100%;
  max-width: 400px;
  height: auto;
}

.card {
  width: 300px;
  padding: 20px;
  border: 1px solid #f08787;
  border-radius: 10px;
  background-color: white;
  transition: box-shadow 0.3s ease, transform 0.3s ease; /* Ajout de la transition pour l'ombre */
}

.card:hover {
  box-shadow: 10px 10px 20px rgba(233, 114, 174, 0.925); 
  transform: translateY(-5px); 
}
</style>
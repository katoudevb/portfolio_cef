<template>
  <div>
    <h1>404 - Page non trouvée</h1>
    <img src="/src/assets/img/erreur.jpg" alt="Image erreur page 404">
    <p>Oups ! La page que vous cherchez n'existe pas.</p>
    <router-link to="/">Retour à l'accueil</router-link>
  </div>
</template>

<style scoped>
.not-found {
  text-align: center;
  padding: 50px;
}

h1 {
  font-size: 48px;
  color: #ff4d4d;
}
p {
  font-size: 18px;
  color: #120101;
}
a {
  display: inline-block;
  margin-top: 20px;
  padding: 10px 20px;
  background: #80a723;
  color: white;
  text-decoration: none;
  border-radius: 5px;
}
a:hover {
  background: green;
  ;
}
</style>

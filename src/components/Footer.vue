<template>
    <footer>
      <div class="footer_social">
        <div class="img">
        <a href="#" target="_blank"><img src="@/assets/img/sociale-2.png" alt="Logo Facebook"></a>
        <a href="#" target="_blank"><img src="@/assets/img/twitter.png" alt="Logo Twitter"></a>
        <a href="https://github.com/katoudevb" target="_blank"><img src="@/assets/img/github.png" alt="Logo GitHub"></a>
        </div>
      </div>
      
      <p>Dernière mise a jour : {{ lastUpdated }}</p>
    <ContactForm/>
    </footer>
  </template>
  
  <script setup>
    import { ref } from "vue";
  import ContactForm from "./ContactForm.vue";
  
    const lastUpdated = ref(new Date().toLocaleDateString());
  </script>
  
  
  <style scoped>
  .footer_social :hover {
          opacity: 50%;
  }
  
  img{
    height: auto;
    width: 30px;
    margin: 1rem;
  }
  
  p{
    margin-bottom: 3rem;
  }
  </style>
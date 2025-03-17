<template>
    <header>
      <img 
          src="@/assets/img/logo.jpg" 
          alt="Logo"
          @click="scrollToTop"
          class="logo"
        />
  
  
      <nav>
          <ul>
              <li><a href="#presentation">Présentation</a></li>
              <li><a href="#projets">Projets</a></li>
              <li><a href="#contact">Contact</a></li>
          </ul>
      </nav>
    </header>
  </template>
  
  <script setup>
    const scrollToTop = () => {
      window.scrollTo({
      top: 0,
      behavior: "smooth",
    });
  };
  </script>
  
  <style scoped>
  img{
          max-width:  90px; 
          height: auto;
  }
  
  nav {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background: #e296d8;
    padding: 10px;
  }
  
  ul {
    display: flex;
    justify-content: center;
    gap: 20px;
    list-style: none;
  }
  
  a {
    color: rgb(220, 239, 156);
    text-decoration: none;
  }
  
  .logo{
      cursor: pointer;
  }
  </style>
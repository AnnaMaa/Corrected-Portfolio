<template>
    <div id="app">
      <!-- Bouton pour ouvrir la modale -->
      <button class="open-modal-btn" @click="openModal">Ouvrir la fenêtre modale</button>
  
      <!-- Fenêtre modale -->
      <div class="modal-overlay" v-if="isModalOpen" @click="closeModal">
        <div class="modal-content" @click.stop>
          <h2>Fenêtre modale</h2>
          <p>Ceci est une fenêtre modale Vue.js.</p>
          <button class="close-btn" @click="closeModal">Fermer</button>
        </div>
      </div>
    </div>
  </template>

  <script>
  export default {
    data() {
      return {
        isModalOpen: false,
      };
    },
    methods: {
      openModal() {
        this.isModalOpen = true;
      },
      closeModal() {
        this.isModalOpen = false;
      },
    },
  };
  </script>

  <style scoped>
  /* Bouton principal */
  .open-modal-btn {
    padding: 1rem 2rem;
    font-size: 1rem;
    background: #3498db;
    color: white;
    border: none;
    cursor: pointer;
    border-radius: 5px;
  }
  
  /* Style de la modale */
  .modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
  }
  
  .modal-content {
    background: white;
    padding: 2rem;
    border-radius: 8px;
    width: 90%;
    max-width: 600px;
    text-align: center;
    position: relative;
  }
  
  /* Bouton de fermeture */
  .close-btn {
    background: #e74c3c;
    color: white;
    padding: 0.5rem 1rem;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    margin-top: 1rem;
  }
  
  .close-btn:hover {
    background: #c0392b;
  }
  </style>
  
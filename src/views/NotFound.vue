
<template>
  <div class="not-found">
    <h1>Erreur 404</h1>
    <p>La page que vous recherchez n'existe pas.</p>
    <router-link to="/">Retour à l'accueil</router-link>
  </div>
</template>

<script>
export default {
  name: "NotFound",
};
</script>

<style scoped>
.not-found {
  text-align: center;
  padding: 50px;
  font-family: Arial, sans-serif;
}

h1 {
  font-size: 3rem;
  color: #e74c3c;
}

p {
  font-size: 1.2rem;
  color: #333;
}

a {
  color: #007bff;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}
</style>

<template>
 <!-- about section design-->
 <section class="about" id="about">
      <div class="about-img">
      <img src="../assets/img/photopro2.jpg" alt="photopro2">  
    </div>

    <div class="about-content">

      <div class="heading">About <span>Me</span></div>
      <h3>Fullstack Developer!</h3>

      <p>Après mes 14 ans de métiers dans la Restauration et Hotellerie j'ai enfin sauté le pas. 
        Cette reconversion me passionne beaucoup.Depuis toute petite je suis passionné d'informatique et de jeux vidéos également. 
        Je suis une personne très minutieuse qui aime le travail bien fait. Une personne organiser et qui aime le travail en équipe.
        Pour ce qui est de ma personnalité je suis une personne très dynamique et passionnée dans tout ce que j'entreprend.
        J'aime le sport, le faite de pouvoir dépasser ses propres limites. Je trouve que cela est très important dans la vie.
        Je n'ai plus qu'une chose à vous dire :
        VIVEZ ET VIBREZ</p>
    
    </div>

    </section>
</template>

<script>
export default {
  name: "About",
};
</script>

<style scoped>
.about {
    display: flex;
    justify-content: center;
    align-items: center ;
    gap: 2rem;
    background: var(--second-bg-color);

}

.about-img img {
    width: 35vw;
}

.heading {
    text-align: center;
    font-size: 4.5rem;

}

.about-content h2   {
    text-align: left;
    line-height: 1.2;
}

.about-content h3 {
    font-size: 2.6rem;
    color: white;

}

.about-content p {
    font-size: 1.6rem;
    margin: 2rem 0 3rem;
    color: white;

}
</style>

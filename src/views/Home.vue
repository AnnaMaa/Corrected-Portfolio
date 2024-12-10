<template>
   <!--home section design-->
   <section class="home" id="home">
      <div class="home-content">
        <h3> Hello, It's Me</h3>
        <h1> Anaïs Maaroufi</h1>
        <h3> And I'm a <span class="multiple-text">{{ currentText }}</span></h3>
        <p>Née en 1992 à Paris. J'ai été avant tout pendant 14 ans dans les metiers de la restaurations et de l'hotellerie.
          Je me suis reconveti dans le digital. Un métier qui me passionne. 
          Vous pouvez voir mes différents projet sur ce site.
        </p>
        
        <div class="social-media">

          <a href="https://www.facebook.com/anna.maaroufi"><i class='bx bxl-meta'></i></a>
          <a href="https://www.instagram.com/anna_moeda_senzala/"><i class='bx bxl-instagram' ></i></a>
          <a href="https://x.com/TsAna4REAL"><i class='bx bxl-twitter' ></i></a>
          <a href="https://github.com/AnnaMaa"><i class='bx bxl-github' ></i></a>
          <a href="https://fr.linkedin.com/in/ana%C3%AFs-maaroufi-9648b2156"><i class='bx bxl-linkedin' ></i></a>
          
        </div>

        <a href="cv/index.html" class="btn"> Download Cv</a>
      </div>

      <div class="home-img">
        <img src="../assets/img/photopro1.jpg" alt="photopro1">
      </div>
    </section>

</template>

<script>


export default {
  name: "Home",
  data() {
   return {
     texts: ['Frontend Developer', 'Backend Developer'], 
     currentIndex: 0,
     currentText: ''
   };
 },
 mounted() {
   this.currentText = this.texts[this.currentIndex];
   this.changeText();
 },
 methods: {
   changeText() {
     setInterval(() => {
       this.currentIndex = (this.currentIndex + 1) % this.texts.length;
       this.currentText = this.texts[this.currentIndex];
     }, 2000); // Change le texte toutes les 2 secondes
   }
 }
};



</script>

<style scoped>




.home-content h3 {
    font-size: 3.2rem;
    font-weight: 700;
}

.home-content h3:nth-of-type(2) {
    margin-bottom: 2rem;

   

}

span {
    color: var(--main-color);

}

.multiple-text {
  font-size: 3.2rem;
  font-weight: bold;
  color:#0ef;
}


.home-content h1 {
    font-size: 5.6rem;
    font-weight: 700;
    line-height: 1.3;
}

.home-content p {
    font-size: 1.6rem;
}

.social-media a {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 4rem;
    height: 4rem;
    background: transparent;
    border: .2rem solid var(--main-color);
    border-radius: 50%;
    font-size: 2rem;
    color: var(--main-color);
    margin: 3rem 1.5rem 3rem 0;
    transition: .5s ease;

}

.social-media a:hover {
    background: var(--main-color);
    color: var(--second-bg-color);
    box-shadow: 0 0 1rem var(--main-color);
}

.btn {
    display:inline-block;
    padding: 1rem 2.8rem;
    background: var(--main-color);
    border-radius: 4rem;
    box-shadow: 0 0 1rem var(--main-color);
    font-size: 1.6rem ;
    color: var(--second-bg-color);
    letter-spacing: .1rem;
    font-weight: 600;
    transition: .5s ease;
}

.btn:hover {
    box-shadow: none;
}

</style>




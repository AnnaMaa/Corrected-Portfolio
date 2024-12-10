<template>
   <!--services section design-->
   <section class="skills" id="skills">
      <h2 class="heading">My <span>Skills</span></h2>
      
      <div class="skills-container">

        <div class="skills-box">
        <i class='bx bx-code-alt' ></i>
          <h3>Hard Skills </h3>
          <p>HTML5</p>
          <p>CSS3</p>
          <p>VUEJS</p>
          <p>GIT et GITHUB</p>
          <p>JAVASCRIPT</p>
          <a href="#" class="btn">Read More</a>
        </div>

          <div class="skills-box">
            <i class='bx bxs-paint' ></i>
            <h3>Soft Skills</h3>
            <p>Organiser</p>
            <p>Dynamique</p>
            <p>Créative</p>
            <p>Aime travailler en équipe</p>
            <p>Polyvalente</p>
            <a href="#" class="btn">Read More</a>
          </div>
        
        </div>
   </section>
   
 <!-- porfolio section design-->
 <section class="portfolio" id="portfolio">
        <h2 class="heading">Latest <span>Project</span></h2>

        <div class="portfolio-container">
          <div class="portfolio-box">
            <img src="../assets/img/pc1.jpg" alt="pc1">
            <div class="portfolio-layer">
              <h4>Présentation du Projet</h4>
              <p>Découvrez la Présentation du Projet
                </p>
                <a href="./Présentation projet/Présentation Projet1.docx"><i class='bx bx-link-external' ></i></a>
              </div>
          </div>

              <div class="portfolio-box">
                <img src="../assets/img/pc2.jpg" alt="pc2">
                <div class="portfolio-layer">
                  <h4>Création de CV</h4>
                  <p> Ci-joint la création de mon cv qui fait parti de ma formation  
                    </p>
                    <a href="./cv/index.html"><i class='bx bx-link-external' ></i></a>
                </div>
            </div>

                  <div class="portfolio-box">
                    <img src="../assets/img/pc3.jpg" alt="">
                    <div class="portfolio-layer">
                      <h4>Création de cahiers des charges</h4>
                      <p> Dans le projet d'une société La Socketterie, J'ai du établir un cahier des charges
                        </p>
                        <a href="./cahier-des-charges/Cahier des charges la socketterie V1.docx"><i class='bx bx-link-external' ></i></a>
                      </div>
                  </div>

                      <div class="portfolio-box">
                        <img src="../assets/img/pc4.jpg" alt="">
                        <div class="portfolio-layer">
                          <h4>Dynamiser un espace commentaire</h4>
                          <p>Vous verrez dans ce document comment dynamiser un espace commentaire
                            </p>
                            <a href="Dynamiser-espace-com-/index.html"><i class='bx bx-link-external' ></i></a>
                          </div>
                      </div>
        </div>
     </section>
  
</template>

<script>
export default {
  name: "Projects",
};
</script>

<style scoped>

.skills h2 {
    margin-bottom: 5rem;

}

.skills-container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    gap : 2rem;
}

.skills-container .skills-box {
    flex: 1 1 30rem;
    background: var(--second-bg-color);
    padding: 3rem 2rem 4rem;
    border-radius: 2rem;
    text-align: center;
    border: .2rem solid var(--bg-color);
    transition: .5s ease;
}

.skills-container .skills-box:hover {
    border-color: var(--main-color);
    transform: scale(1.02);

}

.skills-box i {
     font-size: 7rem;
     color : var(--main-color);

}

.skills-box h3 {
    font-size: 2.6rem;
    color:white;

}


.skills-box p {
    font-size: 1.6rem;
    margin: 1rem 0 3rem;
    color:white;
}

.portfolio {
    background: var(--second-bg-color);

}

.portfolio h2 {
    margin-bottom: 4rem;
}


.portfolio-container {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    align-items: center;
    gap: 2.5rem;
}

.portfolio-container .portfolio-box {
   position: relative;
   border-radius: 2rem;
   box-shadow: 0 0 1rem var(--bg-color);
   overflow: hidden;
   display: flex;

}

.portfolio-box img {
    width: 100%;
    transition: .5s ease;
}

.portfolio-box:hover img{
    transform: scale(1.1);


}


.portfolio-box .portfolio-layer {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(rgba(0, 0, 0, .1), var(--main-color));
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    text-align: center;
    padding: 0 4rem;
    transform: translateY(100%);
    transition: .5s ease;
}

.portfolio-box:hover .portfolio-layer {
    transform: translateY(0);

}

.portfolio-layer h4 {
    font-size: 3rem;
}

.portfolio-layer p {
    font-size: 1.6rem;
    margin: .3rem 0 1rem;
}

.portfolio-layer a {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 5rem;
    height: 5rem;
    background: var(--text-color);
    border-radius: 50%;
}
.portfolio-layer a i {
    font-size: 2rem;
    color: var(--second-bg-color);
}
</style>

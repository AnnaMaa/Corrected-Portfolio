<template>
  
     <!--footer design-->
     <footer class="footer">
      <div class="footer-text">
        <p>© 2024 Tous droits réservés.</p>
        <datetime>20/09/2024</datetime>
      </div>

      <div class="footer-iconTop">
        <a href="#home"><i class='bx bx-up-arrow-alt'></i></a>
      </div>

     </footer>

    
  
</template>

<script>
export default {
  name: "Footer",
};



</script>

<style scoped>
.footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    padding: 2rem 9%;
    background: var(--second-bg-color);

}

.footer-text p {
    font-size: 1.6rem;
    color: white;

}

.footer-iconTop a {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    padding: .8rem;
    background: var(--main-color);
    border-radius: .8rem;
    transition: .5s ease;
}

.footer-iconTop :hover {
    box-shadow: 0 0 1rem var(--main-color);
}

.footer-iconTop a i {
    font-size: 2.4rem;
    color: var(--second-bg-color);

}


.footer-iconTop a {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    padding: .8rem;
    background: var(--main-color);
    border-radius: .8rem;
}

.footer-iconTop a  i {
    font-size: 2.4rem;
    color: var(--second-bg-color);
}
</style>

<script>
  import HeaderApp from './components/HeaderApp.vue';
  export default{
    components: {
      HeaderApp,
    }

  }
</script>

<template>

  <header>
    <HeaderApp></HeaderApp>
  </header>

  <main>
    <div class="container">
      <div class="row">

          <div class="col-33">
              <div class="content p-relative">
                  <img class="main-image" src="./assets/img/1.webp" alt="">
                  <img class="hover-image" src="./assets/img/1b.webp" alt="">

                  <div class="labels">
                      <span class="label red-label">-50%</span>
                      <span class="label green-label">Sostenibilità</span>
                  </div>
                  <div class="description">
                      <div class="brand">Levi's</div>
                      <div class="clothes-name">RELAXED FIT TEE UNISEX</div>
                  </div>
                  <div class="prices">
                      <span class="discount-price">14,99&euro;</span>
                      <span class="original-price">29,99&euro;</span>
                  </div>

              </div>
          </div>

          <div class="col-33">
              <div class="content p-relative">
                  <img class="main-image" src="./assets/img/2.webp" alt="">
                  <img class="hover-image" src="./assets/img/2b.webp" alt="">

                  <div class="labels">
                      <span class="label red-label">-30%</span>
                  </div>
                  <div class="description">
                      <div class="brand">Guess</div>
                      <div class="clothes-name">ROSES TEE</div>
                  </div>
                  <div class="prices">
                      <span class="discount-price">20,99&euro;</span>
                      <span class="original-price">29,99&euro;</span>
                  </div>

              </div>
          </div>

          <div class="col-33">
              <div class="content p-relative">
                  <img class="main-image" src="./assets/img/3.webp" alt="">
                  <img class="hover-image" src="./assets/img/3b.webp" alt="">

                  <div class="labels">
                      <span class="label red-label">-30%</span>
                  </div>
                  <div class="description">
                      <div class="brand">Come Zucchero Filato</div>
                      <div class="clothes-name">VOGLIA DI COLORI PASTELLO</div>
                  </div>
                  <div class="prices">
                      <span class="discount-price">129,99&euro;</span>
                      <span class="original-price">184,99&euro;</span>
                  </div>

              </div>
          </div>

          <div class="col-33">
              <div class="content p-relative">
                  <img class="main-image" src="./assets/img/4.webp" alt="">
                  <img class="hover-image" src="./assets/img/4b.webp" alt="">

                  <div class="labels">
                      <span class="label red-label">-50%</span>
                      <span class="label green-label">Sostenibilità</span>
                  </div>
                  <div class="description">
                      <div class="brand">Levi's</div>
                      <div class="clothes-name">TEE UNISEX</div>
                  </div>
                  <div class="prices">
                      <span class="discount-price">14,99&euro;</span>
                      <span class="original-price">29,99&euro;</span>
                  </div>

              </div>
          </div>

          <div class="col-33">
              <div class="content p-relative">
                  <img class="main-image" src="./assets/img/5.webp" alt="">
                  <img class="hover-image" src="./assets/img/5b.webp" alt="">

                  <div class="labels">
                  </div>
                  <div class="description">
                      <div class="brand">Maya Deluxe</div>
                      <div class="clothes-name">STRIPE BODICE</div>
                  </div>
                  <div class="prices">
                      <span class="discount-price">99,99&euro;</span>
                  </div>

              </div>
          </div>

          <div class="col-33">
              <div class="content p-relative">
                  <img class="main-image" src="./assets/img/6.webp" alt="">
                  <img class="hover-image" src="./assets/img/6b.webp" alt="">

                  <div class="labels">
                      <span class="label green-label">Sostenibilità</span>
                  </div>
                  <div class="description">
                      <div class="brand">Esprit</div>
                      <div class="clothes-name">Maglione - BLACK</div>
                  </div>
                  <div class="prices">
                      <span class="discount-price">29,99&euro;</span>
                  </div>

              </div>
          </div>
      </div>
  </div>
  </main>

  <footer>
    <div class="container">
            
    </div>
  </footer>

</template>

<style>
  *{
      padding:0;
      margin:0;
      box-sizing: border-box;
  }

  body{
      font-family: Arial, Helvetica, sans-serif;
  }

  /*UTILITY*/

  .d-flex{
      display: flex;
  }

  .p-relative{
      position:relative;
  }

  .justify-between{
      justify-content: space-between;
  }

  .align-center{
      align-items: center;
  }

  /*FINE UTILITY*/


  /*LAYOUT*/

  .container{
      max-width:1000px;
      margin: 0 auto;
  }

  header{
      background-color: orange;
      width:100%;
      position:fixed;
      height:40px;
      z-index: 1;
  }

  header .container{
      margin-top:9px;
      color:white;
  }


  main .container{
      padding-top: 55px;
  }

  footer{
      background-color: rgb(40, 40, 40);
      height:70px;
  }

  .row{
      display: flex;
      flex-wrap: wrap;
  }

  .col-33{
      width: calc(100%/3);
  }

  .content{
      margin:10px;
  }

  .content .main-image{
      width: 100%;
      display: block;
  }

  /*FINE LAYOUT*/

  .hover-image {
      width:100%;
      display:none ;
  }

  .col-33:hover .hover-image{
      display: block;
  }

  .col-33:hover .main-image{
      display: none;
  }

  .labels{
      position: absolute;
      bottom:80px;
  }

  .label{
      
      font-size: 0.85em;
      color:white;
      font-weight: bold;
      padding:3px 8px;
  }

  .red-label{
      background-color: red;
  }

  .green-label{
      background-color: green;
  }

  .brand{
      font-size: 0.75em;
  }

  .clothes-name{
      font-weight: bold;
  }

  .prices{
      font-size: 0.80em;
  }

  .discount-price{
      color:red;
      font-weight: bold;
  }

  .original-price{
      text-decoration: line-through;
  }

  .logo{
      width:100px;
      height:auto;
  }
</style>

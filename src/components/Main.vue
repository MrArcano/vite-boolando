<script>
export default {
  name: "Main"
}
</script>

<template>
  
  <main>
    <div class="container">
      <div class="cards flex-box">

        
        <div class="card"> <!-- inizio card -->
          <div class="card-top">
            <div class="card-image">
              <img src="../assets/img/1.webp" alt="img1">
              <img src="../assets/img/1b.webp" alt="img1b">
            </div>
            <div class="hearth">
              <span>&hearts;</span>
            </div>
            <div class="badge-box">
              <span class="badge badge-red">-50%</span>
              <span class="badge badge-green">Sostenibilità</span>
            </div>
          </div>

          <div class="card-bot">
            <span class="brand block-box">Levi's</span>
            <span class="name-item block-box">Relaxed Fit Tee Unisex</span>
            <span class="new-price">14,99&euro;</span>
            <span class="old-price">29,99&euro;</span>
          </div>
        </div> <!-- fine card -->

        <div class="card"> <!-- inizio card -->
          <div class="card-top">
            <div class="card-image">
              <img src="../assets/img/2.webp" alt="img2">
              <img src="../assets/img/2b.webp" alt="img2b">
            </div>
            <div class="hearth">
              <span>&hearts;</span>
            </div>
            <div class="badge-box">
              <span class="badge badge-red">-30%</span>
            </div>
          </div>

          <div class="card-bot">
            <span class="brand block-box">Guess</span>
            <span class="name-item block-box">Roses Tee</span>
            <span class="new-price">20,99&euro;</span>
            <span class="old-price">29,99&euro;</span>
          </div>
        </div> <!-- fine card -->

        <div class="card"> <!-- inizio card -->
          <div class="card-top">
            <div class="card-image">
              <img src="../assets/img/3.webp" alt="img3">
              <img src="../assets/img/3b.webp" alt="img3b">
            </div>
            <div class="hearth">
              <span>&hearts;</span>
            </div>
            <div class="badge-box">
              <span class="badge badge-red">-30%</span>
            </div>
          </div>

          <div class="card-bot">
            <span class="brand block-box">Come Zucchero Filato</span>
            <span class="name-item block-box">Voglia di colori pastello</span>
            <span class="new-price">129,99&euro;</span>
            <span class="old-price">184,99&euro;</span>
          </div>
        </div> <!-- fine card -->

        <div class="card"> <!-- inizio card -->
          <div class="card-top">
            <div class="card-image">
              <img src="../assets/img/4.webp" alt="img4">
              <img src="../assets/img/4b.webp" alt="img4b">
            </div>
            <div class="hearth">
              <span>&hearts;</span>
            </div>
            <div class="badge-box">
              <span class="badge badge-red">-50%</span>
              <span class="badge badge-green">Sostenibilità</span>
            </div>
          </div>

          <div class="card-bot">
            <span class="brand block-box">Levi's</span>
            <span class="name-item block-box">Tee Unisex</span>
            <span class="new-price">14,99&euro;</span>
            <span class="old-price">29,99&euro;</span>
          </div>
        </div> <!-- fine card -->

        <div class="card"> <!-- inizio card -->
          <div class="card-top">
            <div class="card-image">
              <img src="../assets/img/5.webp" alt="img5">
              <img src="../assets/img/5b.webp" alt="img5b">
            </div>
            <div class="hearth">
              <span>&hearts;</span>
            </div>
          </div>

          <div class="card-bot">
            <span class="brand block-box">Maya Deluxe</span>
            <span class="name-item block-box">Stripe Bodice</span>
            <span class="new-price">99,99&euro;</span>
          </div>
        </div> <!-- fine card -->

        <div class="card"> <!-- inizio card -->
          <div class="card-top">
            <div class="card-image">
              <img src="../assets/img/6.webp" alt="img6">
              <img src="../assets/img/6b.webp" alt="img6b">
            </div>
            <div class="hearth">
              <span>&hearts;</span>
            </div>
            <div class="badge-box">
              <span class="badge badge-green">Sostenibilità</span>
            </div>
          </div>

          <div class="card-bot">
            <span class="brand block-box">Esprit</span>
            <span class="name-item block-box">Maglione - Black</span>
            <span class="new-price">29,99&euro;</span>
          </div>
        </div> <!-- fine card -->

      </div>
    </div>
  </main>

</template>

<style lang="scss" scoped>
  /* MAIN */
  /* ---------------------------------------------------------- */
  main{
    margin-top: 70px;
  }

  .cards{
    padding-top: 60px;
    flex-wrap: wrap;
    justify-content: center;
  }

  .card{
    cursor: pointer;
    width: calc((100% - 48px) / 3);
    min-width: 250px;
    margin-right: 16px;
  }

  .card-top{
    max-width: 450px;
    position: relative;
  }
  /* ---------------------------------------------------------- */

  /* CARD IMAGE */
  /* ---------------------------------------------------------- */

  .card-image img:last-of-type{
    position: absolute;
    top: 0;
    left: 0;
    display: none;
  }

  .card-image:hover img:last-of-type{
    display: inline-block;
  }
  /* ---------------------------------------------------------- */

  /* HEARTH */
  /* ---------------------------------------------------------- */
  .hearth{
    position: absolute;
    top: 16px;
    right: 0;

    height: 50px;
    width: 50px;

    line-height: 50px;
    text-align: center;

    background-color: white;
    font-size: 20px;
  }

  .hearth:hover{
    color: red;
  }
  /* ---------------------------------------------------------- */

  /* BADGE */
  /* ---------------------------------------------------------- */
  .badge-box{
    width: 100%;
    position: absolute;
    bottom: 50px;
  }

  .badge{
    color: white;
    padding: 4px 12px;
    font-weight: bold;
  }

  .badge-red{
    background-color: red;
  }

  .badge-green{
    background-color: green;
  }
  /* ---------------------------------------------------------- */

  /* CARD BOT */
  /* ---------------------------------------------------------- */
  .card-bot{
    padding-bottom: 50px;
  }

  .brand{
    font-size: 14px;
  }

  .name-item{
    text-transform: uppercase;
    font-size: 18px;
    font-weight: bold;
  }

  .new-price{
    color: red;
    font-weight: bold;
    padding-right: 8px;
  }

  .old-price{
    text-decoration: line-through;
  }
  /* ---------------------------------------------------------- */
</style>
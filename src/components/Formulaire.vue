<script setup lang="ts">

</script>

<template>
  <div class="formulaire">
    <h3>Pour participer, entrez vos informations et jouez !</h3>
    <form action="">
      <div class="form-grid">
        <div class="form-cat">
          <label class="to-complete" for="lastname">Nom*</label>
          <input type="text" id="lastname" name="lastname" required>
        </div>
        <div class="form-cat">
          <label class="to-complete" for="name">Prénom*</label>
          <input type="text" id="name" name="name" required>
        </div>
        <div class="form-cat">
          <label class="to-complete" for="email">Email*</label>
          <input type="text" id="email" name="email" required>
        </div>
        <div class="form-cat">
          <label class="to-complete" for="phone-number">Numéro de téléphone</label>
          <input type="text" id="phone-number" name="phone-number">
        </div>
      </div>
      <div class="form-check">
        <label class="to-check" for="subscribe">En participant à ce jeu, vous acceptez de recevoir des offres d'emplois d'Amaelles et toutes informations relatives à nos actions de recrutement</label>
        <input type="checkbox" id="subscribe" name="subscribe">
      </div>
      <div class="form-check">
        <label class="to-check" for="subscribe">En cochant cette case, vous consentez à ce que vos données personnelles soient collectées et partagées avec les structures membres du collectif Amaelles. Elles seront utilisées à des fins de statistiques et pour les actions menées à des fins de recrutement. Ces données seront conservées pendant deux ans.</label>
        <input type="checkbox" id="subscribe" name="subscribe" required>
      </div>
      <button @click.prevent="">Je participe !</button>
    </form>
  </div>
</template>

<style lang="scss" scoped>
@import "/public/styles/variables.scss";

.formulaire {
  h3 {
    text-align: center;
    margin-bottom: 24px;
    padding: 0 12px;
    font-family: "Playfair Display Variable", serif;
    font-weight: 800;
    @media screen and (min-width: $m-screen) {
      text-align: left;
      font-size: 20px;
      padding: 0;
    }
  }
  form {
    display: flex;
    flex-direction: column;
    @media screen and (min-width: $m-screen){
      .form-grid {
        display: grid;
        grid-template-columns: repeat(6, 1fr);
        grid-template-rows: repeat(2, 1fr);
        grid-column-gap: 20px;
        grid-row-gap: 20px;
        align-items: center;
        .form-cat:nth-child(1) {
          grid-area: 1 / 1 / 2 / 4;
        }
        .form-cat:nth-child(2) {
          grid-area: 1 / 4 / 2 / 7;
        }
        .form-cat:nth-child(3) {
          grid-area: 2 / 1 / 3 / 5;
        }
        .form-cat:nth-child(4) {
          grid-area: 2 /5 /3 /7;
        }
      }
    }
  }
  .form-cat {
    display: flex;
    flex-direction: column;
    margin: 16px 0;

    label.to-complete {
      margin-bottom: 12px;
      color: #4D4D4D;
    }

    input[type="text"] {
      border: inherit;
      background-color: #F4F4F4;
      border-radius: 12px;
      box-shadow: $basic-shadow;
      padding: 8px 12px;
    }
  }
  .form-check {
    display: flex;
    flex-direction: row-reverse;
    align-items: flex-start;
    justify-content: flex-end;
    margin: 16px 0;
    label.to-check {
      font-weight: 200;
      font-size: 12px;
      font-style: italic;
    }
    input[type="checkbox"] {
      margin: 4px 16px 0 12px;
      transform: scale(1.4);
    }
  }
  button {
    margin: 24px auto;
  }
}

</style>
<script setup lang="ts">

</script>

<template>
  <div class="formulaire">
    <h3>Pour participer, entrez vos informations et jouez !</h3>
    <form action="">
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
      <div class="form-check">
        <label class="to-check" for="subscribe">En cochant cette case, vous acceptez de recevoir des <strong>offres
          liés aux
          services d’Amaelles et aux jobs d’été proposés par l’association.</strong></label>
        <input type="checkbox" id="subscribe" name="subscribe">
      </div>
      <div class="form-check">
        <label class="to-check" for="subscribe">En cochant cette case, vous consentez à ce que vos données personnelles soient collectées
          et utilisées à des fins informatives dans le cadre du jeu concours. Ces données seront conservées pendant une
          année.*</label>
        <input type="checkbox" id="subscribe" name="subscribe" required>
      </div>
      <button @click.prevent="">Je participe !</button>
    </form>
  </div>
</template>

<style lang="scss" scoped>
@import "../../public/styles/variables.scss";

.formulaire {
  h3 {
    text-align: center;
    margin-bottom: 24px;
    padding: 0 12px;
    font-family: "Playfair Display Variable", serif;
    font-weight: 800;
  }
  form {
    display: flex;
    flex-direction: column;
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
    justify-content: flex-start;
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
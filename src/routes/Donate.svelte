<script>
  import qrTwint from '$lib/images/association/qr-twint.png';
</script>

<section class="donate">
  <div class="container">
    <h2>Aidez nous</h2>
    <div class="card">
      <h3>Pour soutenir le projet:</h3>
      IBAN: CH53 0076 7000 S546 2495 4<br>
      Numéro TWINT : 078 958 06 26
    </div>
    <p>
      <img src={qrTwint} width="200" height="200" />
    </p>
  </div>
</section>

<style lang="sass">
  .donate
    h2
      font-family: 'Anton', sans-serif
      font-weight: 400
      font-size: 24px
      text-transform: uppercase
      line-height: 1
      margin: 0
      text-align: center

    p
      margin: 40px 0
      font-size: 18px
      font-weight: 500
      line-height: 30px
      text-align: center

    .card
      text-align: center
      line-height: 24px
</style>
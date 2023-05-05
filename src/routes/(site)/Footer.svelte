<script>
  import logo from '$lib/images/logo-white.webp';
  import Icon from '@iconify/svelte';
</script>

<div class="border-top"></div>

<section id="footer">
  <div class="container">
    <div class="content">
      <div class="content-left">
        <div id="logo">
          <a href="/new"><img src={logo} alt="Logo" /></a>
        </div>

        <p>Association basée à Lausanne (Suisse)</p>
        <p><a href="mailto:info@outcha.org">Contactez-nous</a></p>
      </div>

      <div class="content-right">
        <div class="social">
          <h4>Suivez-nous</h4>
          <ul>
            <li>
              <a href="https://www.facebook.com/outchaswitzerland" target="_blank">
                <span class="icon"><Icon icon="mdi:facebook" /></span>
              </a>
            </li>
            <li>
              <a href="https://www.youtube.com/@Outcha" target="_blank">
                <span class="icon"><Icon icon="mdi:youtube" /></span>
              </a>
            </li>
            <li>
              <a href="https://www.instagram.com/out_cha_association/" target="_blank">
                <span class="icon"><Icon icon="mdi:instagram" /></span>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>

  </div>
</section>

<div id="post-footer">
  <span class="icon icon-lg"><Icon icon="ph:code-bold" /></span> with
  <span class="icon"><Icon icon="mdi:cards-heart" /></span> by
  <a href="https://cyrilsuzat.com" target="_blank">Cyril Suzat</a>
</div>

<style lang="sass">
  .border-top
    background: url("../../lib/images/border-blue-top.webp") repeat-x center top
    height: 80px

  #footer
    background-color: $tertiary
    padding: 40px 0
    color: #a1a4ac

  .content
    display: flex
    flex-direction: column
    justify-content: space-between
    align-items: center
    text-align: center

    +tablet
      flex-direction: row
      text-align: left

  p
    margin: 1rem 0

  a
    color: #fff
    transition: all 200ms ease

    &:hover
      color: $secondary

  #logo
    img
      height: 70px

  .social
    display: flex
    align-items: center
    margin: 10px 0

    h4
      text-transform: uppercase
      font-size: 16px
      font-weight: bold
      letter-spacing: -1px
      margin-right: 16px

    ul
      display: flex
      margin: 0
      padding: 0
      list-style: none

      li
        margin: 0 8px

    .icon
      font-size: 50px

    a
      color: #eee

      &:hover
        color: #ca2b14

  #post-footer
    background-color: #ca2b14
    color: #fff
    font-size: 12px
    text-align: center
    padding: 0 0 4px 0

    .icon
      font-size: 13px
      position: relative
      bottom: -3px

      &.icon-lg
        font-size: 15px

    a
      text-decoration: none
      border-bottom: dotted 1px

      &:hover
        color: #fff
        border-bottom: none
</style>
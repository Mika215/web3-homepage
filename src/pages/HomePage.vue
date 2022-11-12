<template>
  <div class="alami-home-page">
    <header class="alami-home-page__header">
      <div class="alami-home-page__logo">W.Logo</div>
      <ul 
        v-for="(item,i) in menuItems"
        :key="i"
        class="alami-home-page__menu">
        <li class="alami-home-page__menu-item">{{item.label}}</li>
      </ul>
    </header>
    <main class="alami-home-page__main">
      <section class="alami-home-page__news-block">
        <div class="alami-home-page__news-left">
          <figure class="alami-home-page__image-container">
            <img src="" alt="" class="alami-home-page__img">
          </figure>
          <article class="alami-home-page__content-container">
            <h3 class="alami-home-page__contnet-title">The Brigt Future of Web 3.0?</h3>
            <div class="alami-home-page__content-group">
              <div class="alami-home-page__content">
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dignissimos, quo quaerat eaque soluta neque, laudantium doloremque illo vitae nostrum unde ipsa enim cupiditate molestias, eum ad laboriosam vero voluptatibus! Temporibus!</p>
              </div>
              <button class="alami-home-page__read-more">Read More</button>
            </div>
          </article>
        </div>
        <article class="alami-home-page__news-right">
          <article class="alami-home-page__right-wrapper">
            <h3 class="alami-home-page__right-title">New</h3>
              
              <div class="alami-home-page__right-content">
                <h5>Hydrogen VS Electric Cars</h5>
                <p>Lorem ipsum dolor sit amet consectetur 
                  adipisicing elit. Dignissimos, 
                  quo quaerat eaque soluta neque, laudantium doloremque 
                  illo vitae nostrum unde ipsa enim cupiditate molestias, eum ad laboriosam vero voluptatibus! Temporibus!</p>
              </div>

              <div class="alami-home-page__right-content">
                <h5>The Downside of AI Artistry</h5>
                <p>Lorem ipsum dolor sit amet consectetur 
                  adipisicing elit. Dignissimos, 
                  quo quaerat eaque soluta neque, laudantium doloremque 
                  illo vitae nostrum unde ipsa enim cupiditate molestias, eum ad laboriosam vero voluptatibus! Temporibus!</p>
              </div>

              <div class="alami-home-page__right-content">
                <h5>is VC Funding Drying Up?</h5>
                <p>Lorem ipsum dolor sit amet consectetur 
                  adipisicing elit. Dignissimos, 
                  quo quaerat eaque soluta neque, laudantium doloremque 
                  illo vitae nostrum unde ipsa enim cupiditate molestias, eum ad laboriosam vero voluptatibus! Temporibus!</p>
              </div>
            
          </article>
        </article>
      </section>
      <div class="alami-home-page__ellipses-block">
        <article class="alami-home-page__ellipses-item">
          <div class="alami-home-page__ellipses-item-image-container">
            <img class="alami-home-page__ellipses-item-img"  src="/mds" alt="">
          </div>
          <div class="alami-home-page__ellipses-item-content">
            <span class="alami-home-page__ellipses-item-code">01</span>
            <h6 class="alami-home-page__ellipses-item-title">Reviving Retro Pcs</h6>
          <p class="alami-home-page__ellipses-item-desc">Lorem ipsum dolor sit amet.</p>
          </div>
        </article>
        <article class="alami-home-page__ellipses-item">
          <div class="alami-home-page__ellipses-item-image-container">
            <img class="alami-home-page__ellipses-item-img"  src="/sshd" alt="">
          </div>
          <div class="alami-home-page__ellipses-item-content">
            <span class="alami-home-page__ellipses-item-code">02</span>
            <h6 class="alami-home-page__ellipses-item-title">Reviving Retro Pcs</h6>
          <p class="alami-home-page__ellipses-item-desc">Lorem ipsum dolor sit amet.</p>
          </div>
        </article>
        <article class="alami-home-page__ellipses-item">
          <div class="alami-home-page__ellipses-item-image-container">
            <img class="alami-home-page__ellipses-item-img"  src="/sd" alt="">
          </div>
          <div class="alami-home-page__ellipses-item-content">
            <span class="alami-home-page__ellipses-item-code">03</span>
            <h6 class="alami-home-page__ellipses-item-title">Reviving Retro Pcs</h6>
          <p class="alami-home-page__ellipses-item-desc">Lorem ipsum dolor sit amet.</p>
          </div>
        </article>
      </div>
    </main>
    <footer class="alami-home-page__footer"></footer>

  </div>
</template>

<script>
  export default{
    name:'HomePage',

    computed:{
      menuItems(){
        return [
          {
            label:'Home',
          },
          {
            label:'New',
          },
          {
            label:'Popular',
          },
          {
            label:'Trending',
          },
          {
            label:'Categories',
          },
        ]
      }
    }
  }
</script>
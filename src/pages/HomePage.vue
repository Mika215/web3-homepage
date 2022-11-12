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
          <h3 class="alami-home-page__right-title">New</h3>  
          <article 
            v-for="(topic,k) in newTopics"
            :key="k"
            class="alami-home-page__right-wrapper">
              <div class="alami-home-page__right-content">
                <h5>{{topic.title}}</h5>
                <p>{{topic.description}}</p>
              </div>    
          </article>
        </article>
      </section>
      <div 
        v-for="(entry,j) in newsCollection"
        :key="j"
        class="alami-home-page__ellipses-block">
        <article class="alami-home-page__ellipses-item">
          <div class="alami-home-page__ellipses-item-image-container">
            <img class="alami-home-page__ellipses-item-img"  :src="getImageUrl(entry.src)" :alt="entry.src">
          </div>
          <div class="alami-home-page__ellipses-item-content">
            <span class="alami-home-page__ellipses-item-code">{{entry.code}}</span>
            <h6 class="alami-home-page__ellipses-item-title">{{entry.title}}</h6>
          <p class="alami-home-page__ellipses-item-desc">{{entry.description}}</p>
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
      },

      newsCollection(){
        return [
          {
            code:'01',
            description:'What happenes when old Pcs are given modern upgrades?',
            src:'image-retro-pcs',
            title:'Reviving Retro PCs',
          },
          {
            code:'02',
            description:'Our best picks for various needs and budgets',
            src:'image-top-laptops',
            title:'Top 10Laptops of 2022',
          },
          {
            code:'03',
            description:'How the pandemic has spaked fresh opportunities',
            src:'image-gaming-growth',
            title:'The Growth of Gaming',
          },
        ]
      },

      newTopics(){
        return [
          {
            description:'Will hydrogen-fueled cars ever catch up to EVs?',
            title:'Hydrogen VS Electric Cars',
          },
          {
            description:'What are the possible adverse effects of on-demand AI image generator?',
            title:'The Downside of AI Artistry',
          },
          {
            description:'Private funding by VC firms is down 50% YOY.We take a look at what that means. ',
            title:'Is VC Funding Drying Up?',
          },
        ]
      },
    },

    methods :{

      getImageUrl(path){
        return require(`../assets/images/${path}.jpg`);
      },
    }
  }
</script>
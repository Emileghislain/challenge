<template>
  <nav class="container">
    <div class="logo">
      <span>Skillex</span>
      <span class="logo__span"></span>
    </div>
    <ul class="navigation">
      <li class="navigation__menu">Find passion</li>
      <li class="navigation__menu">Categories</li>
      <li class="navigation__menu">Skills</li>
      <li class="navigation__menu">Customers</li>
    </ul>
    <div class="button">
      <span class="button__login">Login</span>
      <button class="button__free">Free Trial</button>
    </div>
  </nav>
  <main class="container__body">
    <div class="left">
      <h1>
        <span class="appear"><span>Watch.</span></span>
        <span class="appear"><span>Learn.</span></span>
        <span class="appear"><span>Grow.</span></span>
      </h1>
      <div class="search">
        <input placeholder="Find your passion"/>
        <button>Go</button>
      </div>
    </div>
    
    <div class="right">
      <div class="image" style="background-image: url('/images/pexels-lina-kivaka-1661575.jpg')">
        <div class="image__writing">Writing</div>
        <div class="text">
          <div class="">Writing <br/>Course</div>
          <div class="image__bloc">
            <div class="image__bloc__100">100</div>
            <div class="image__bloc__topic">Topics</div>
          </div>
        </div>
      </div>
      <div class="image" style="background-image: url('/images/pexels-reign-martinez-11720281.jpg')">
        <div class="image__writing">Writing</div>
        <div class="text">
          <div class="">Writing <br/>Course</div>
          <div class="image__bloc">
            <div class="image__bloc__100">100</div>
            <div class="image__bloc__topic">Topics</div>
          </div>
        </div>
      </div>
      <div class="image" style="background-image: url('/images/pexels-lina-kivaka-1661575.jpg')">
        <div class="image__writing">Writing</div>
        <div class="text">
          <div class="">Writing <br/>Course</div>
          <div class="image__bloc">
            <div class="image__bloc__100">100</div>
            <div class="image__bloc__topic">Topics</div>
          </div>
        </div>
      </div>
    </div>
  </main>
    <div class="second">
      <div class="second__title">
        <span>Unlimited access to 100+ instructors.</span>
      </div>
      <ul class="second__section">
        <li class="second__section__1">
          All categories
        </li>
        <li class="second__section__2">Entertainment
          <span></span>
        </li>
        <li class="second__section__3">Lifestyle<span></span></li>
        <li class="second__section__4">Writing<span></span></li>
        <li class="second__section__5">Business<span></span></li>
        <li class="second__section__6">Food<span></span></li>
      </ul>
      
    </div>
    <div class="card">
      <div class="card__1">
        <div class="image" style="background-image: url('/images/pexels-lina-kivaka-1661575.jpg')">
          <span class="span__circle"></span>
        </div>
        <div class="text"> 
          <span class="text__1">Sales Marketing</span>
          <span class="text__2">4 month</span>
        </div>
      </div>
      <div class="card__2">
        <div class="image" id="image" style="background-image: url('/images/pexels-lina-kivaka-1661575.jpg')">
          <span class="span__circle"></span>
        </div>
        <div class="text"> 
          <span class="text__1">Sales Marketing</span>
          <span class="text__2">4 month</span>
        </div>
      </div>
      <div class="card__3">
        <div class="image" style="background-image: url('/images/pexels-lina-kivaka-1661575.jpg')">
          <span class="span__circle"></span>
        </div>
        <div class="text"> 
          <span class="text__1">Sales Marketing</span>
          <span class="text__2">4 month</span>
        </div>
      </div>
      <div class="card__4">
        <div class="image" style="background-image: url('/images/pexels-lina-kivaka-1661575.jpg')">
          <span class="span__circle"></span>
        </div>
        <div class="text"> 
          <span class="text__1">Sales Marketing</span>
          <span class="text__2">4 month</span>
        </div>
      </div>
    </div>
    <img src="/images/pexels-lina-kivaka-1661575.jpg"/>
</template>

<script>
export default {
  name: 'MyHeader',
  data(){
    return{
      prevRat : 0
    }
  },

  mounted() {
    let observer = new IntersectionObserver((entries)=>{
      entries.forEach((entry)=>{
        console.log(entry)
        if(this.prevRat < entry.intersectionRatio){
          console.log('prevRat < entry.intersectionRatio')
        }else{
          console.log('prevRat > entry.intersectionRatio')
        }
        console.log('prevRat ', this.prevRat)
        console.log('entry.intersectionRatio', entry.intersectionRatio)
        this.prevRat = entry.intersectionRatio
      })
    });
    const elemnts = document.getElementById('image');
    observer.observe(elemnts);
  },

}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import '../assets/css/header.scss';
</style>

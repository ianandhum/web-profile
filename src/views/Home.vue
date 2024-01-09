<template>
  <main>
    <article>
      <header>
        <h1>Hi, I'm <strong>Anandhu</strong></h1>
      </header>
      <section>
        <h2 class="eye-catch"><sup>focusing on:</sup>🌐👨🏽‍💻&nbsp;&nbsp;&nbsp;&nbsp;<sup>intersted in:</sup>🧪⚛🌌🚀</h2>
      </section>
      <section class="links">
          <a v-for="profile in profiles" v-bind:key="profile.id" v-bind:href="profile.link" class="link">
              <div class="link-img" v-bind:style="{'background-image':'url('+profile.icon+')'}"></div>
              <div class="link-text">{{profile.text}}</div>
          </a>
      </section>
    </article>
  </main>
</template>

<style lang="scss" scoped>

  @import '../scss/variables';
  main{
    width:100vw;
    display: flex;
    flex-direction: column;
    font-family:'Courier New', Courier, monospace
  }
  header{
    margin-top:30vh;
    padding:50px 0;
    h1{
      text-align:center;
    }
    
  }
  section{
    padding: 10px 0;

    h2.eye-catch {
      font-size: 3em;
      font-weight: 400;
      margin :0;
      text-align: center;
    }

    h2.eye-catch sup {
      font-size: 0.4em;
    }
  }
  section.links {
    display: flex;
    justify-content: center;
  }
  .link{
      height: auto;
      width:auto;
      margin:30px 20px;
      float: left;
      text-decoration: none;
      .link-img{
          border-radius: 50%;
          -moz-border-radius: 50%;
          -webkit-border-radius: 50%;
          -o-border-radius: 50%;
          -ms-border-radius: 50%;
          border:2px solid $color;
          height:50px;
          width:50px;
          background-size: cover;
          background-origin: center center;
          background-color:#fff;
      }
      .link-text{
          color:$color;
          text-align: center;
          margin-top:8px;
      }
  }
</style>


<script>
export default {
  name: 'home',
  data:function(){
    return{
      profiles:[
        {
          id:1,
          link:"https://dev.to/ianandhum",
          icon:"/static/devto.png",
          text:"Dev.to"
        },
        {
          id:2,
          link:"https://linkedin.com/in/ianandhum",
          icon:"/static/ln.png",
          text:"LinkedIn"
        },
        {
          id:3,
          link:"https://github.com/ianandhum",
          icon:"/static/github.svg",
          text:"Github"
        }
      ]
    }
  }
}
</script>

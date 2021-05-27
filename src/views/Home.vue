<template>
  <main>
    <article>
      <header>
        <h1>Hi, I'm <strong>Anandhu</strong></h1>
      </header>
      <section>
        <h2 class="eye-catch">Passion = 👨🏽‍💻</h2>
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
    font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  }
  header{
    margin-top:30vh;
    h1{
      text-align:center;
    }
    
  }
  section{
    h2.eye-catch {
      font-size: 5em;
      font-weight: 200;
      margin :0;
      text-align: center;
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
          link:"https://dev.to/anandhumanoj",
          icon:"/static/devto.png",
          text:"Dev.to"
        },
        {
          id:2,
          link:"https://linkedin.com/in/anandhumanoj",
          icon:"/static/ln.png",
          text:"LinkedIn"
        },
        {
          id:3,
          link:"https://github.com/anandhumanoj",
          icon:"/static/github.svg",
          text:"Github"
        }
      ]
    }
  }
}
</script>

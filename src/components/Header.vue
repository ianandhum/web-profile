<template>
    <header>
      <nav>
        <!-- <div class="logo">
            
        </div> -->
        <div class="spacer"></div>
        <ul>
          <li><router-link to="/">Home</router-link></li>
          <li><router-link to="/about">About</router-link></li>
        </ul>
      </nav>
    </header>
</template>

<style lang="scss" scoped>
    header{
        box-shadow: 1px 1px 20px rgba(0, 0, 0, 0.04);
    }
    nav{
        display: flex;
        height:100%;
        
        /* div.logo{
            background-color: #000;
            color:#fff;
            flex-basis: 100px;
            display: flex;
            justify-content: center;
            flex-direction: column;
            text-align: center;
        } */
        div.spacer{
            flex-grow: 1;
        }
        ul{
            list-style: none;
            display: flex;
            padding-left: 0px;
            margin:0 10px 0 0;
            li{
                padding:20px;
                &:hover{
                    background-color:#000;
                    a{
                        color:#fff;
                    }
                }
                a{
                    color:#000;     
                    text-decoration: none;
                    
                }

            }
        }
    }
    
</style>

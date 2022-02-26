<template>

  <main class="maine">

     <div>   
       
       <div v-show="!mobile" class="desktop">
         <header class="desktoptext">
          <h1 class="desktopheader1">Hello, my name is Samson, also known as </h1>
          <h1 class="desktopheader2">Snootnoot</h1>
          <p class ="hobbies">I like to sit in my room all day and procastinate.</p>   
         </header>
         <div class="iconz">
         <a href="https://github.com/Snootnoot" target="_blank" rel="noopener noreferrer">
         <img class="icon" src="./assets/github.png">
          </a>
          <a href="https://insertdevname.itch.io/" target="_blank" rel="noopener noreferrer">
         <img class="icon" src="./assets/itch.png">
          </a>
          <a href="https://www.youtube.com/channel/UCIVusMqdNHxLKt9LFySguFQ" target="_blank" rel="noopener noreferrer">
         <img class="icon" src="./assets/yt.png">
          </a>
         </div>
         <header class="bottext">
         <p class="para">Currently working on:</p>
         <h1 class="heads">Nothing.</h1>
         </header>
       </div>

    
        
     <div v-show="mobile" class="mobilenavbar">
       
          <header class="mobileheader">
            <h1 class="mobiletext">
                asdas
            </h1>wwwwwwwwwwwwwwwww
          </header>
                           
        <ul class="footer"> 
             <li>
                <div class="mobilebutton">
                    <Button text="New" class="btn4"/>  
                    <Button text="Best" class="btn5"/>
                    <Button text="Old" class="btn6"/>
                </div>
              </li>
        </ul>
      </div>  
    </div>  
  </main>
         
</template>

<script>
import Header from './components/Header.vue'
import Button from './components/PFContent.vue'
export default {
    name: 'Header',
 
    props:   {
        title: String,
    },
    components:
    {
        Button,
    },
  
        Header,  data()
    {
      return{
        mobile: false,
        windowWidth: null,
      }
    }
}
</script>
//TODO: add phone switch support to top bar
<style scoped>
  
  .bottext{
    color: wheat;
    font-size: 1vw;
    text-align: center;
  }
  .heads{
    padding: 0;
    text-decoration: underline;
    text-decoration-color: #e6b566;
  }
  .icon{
    transition: all .5s ease;
    width: 4vmax;
    height: 4vmax;
    padding: 15px;   
  }
   .icon:hover{
     transition: all .7s ease;
    width: 4vmax;
    height: 4vmax;
    padding: 15px; 
    opacity: 50%;  
  }

  .iconz{
    width: 4vmax;
    height: 4vmax;
    padding: 1vw; 
    position: absolute;
    display: flex;
    left: 15vw;
    position: absolute;
      top: 110%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 100%;
      text-align: left;
      justify-content: center;
  }


  .mobileheader{
    position: -webkit-sticky;
    position: sticky;
    list-style-type: none;  
    width: 100%;
    max-width: 100%;
    height: 0px;
    border: 0px;
    padding:0px;
    margin:0px;
    top: 0;
    left: 0;
  }

    .desktopheader4{
      
      border: .5px solid wheat;
      border-radius: 0px 0px 0px 0px;
      padding: 5px; 
      text-align: center;
      margin-left: 1vw;
      
      
    }

    .desktopheader1, .desktopheader2{
      
      text-align: center;
      font-size: 2vmax;
      width: 100%;
    }

    .desktopheader2{
      border: 5px dotted;
      padding-left: 10px;
      padding-right: 10px;
      display: inline; 
      text-align: center;
      border-color: #e5707e;
      margin-left: 14.5vw;

    }

     .hobbies{
    
      text-align: center;
      font-size: 1.2vmax;
      padding-top: 5px;
      }
  

    .desktoptext{
      color:wheat;
      
    }



    .mobiletext{
     
      font-size: 5vw;
      
    }

    .desktop{
      position: absolute;
      top: 40%;
      left: 50%;
     
      transform: translate(-50%, -50%);
      font-size: 100%;
      text-align: left;
      justify-content: center;
    }
  
   .button{
    margin: 0;
    position: absolute;
    display: flex;
    top: 50%;
    left: 50%;
    -ms-transform: translate(-50%, -50%);
    transform: translate(-50%, -50%);
    overflow: hidden;
    padding: 0px;
    font-family: 'Roboto', sans-serif;
    margin-left: 100px;
    margin-right: 1px;
    padding-left: 20px;
    width: 500px;
    font-size: 2vw;
    max-width: 100%;
    }
     .btn1{
      transition: 0.4s ease all;
      border-left: 1px solid transparent;
      padding: 0 0 4px;
    }
      .btn1:hover{
        transition: 0.4s ease all;
        border-left: 1px solid rgb(206, 205, 205);
        width: 25%;
      }
    
      .btn2{
      transition: 0.4s ease all;
      border-left: 1px solid transparent;
      padding: 0 0 4px;
    }
      .btn2:hover{
        transition: 0.4s ease all;
        border-left: 1px solid rgb(206, 205, 205);
        width: 25%;
      }

      .btn3{
      transition: 0.4s ease all;
      border-left: 1px solid transparent;
      padding: 0 0 4px;
    }
      .btn3:hover{
        transition: 0.4s ease all;
        border-left: 1px solid rgb(206, 205, 205);
        width: 25%;
      }
  .footer{
    position: fixed;
    list-style: none;
    left: 0;
    bottom: 0;
    width: 100%;
    max-width: 100%;
    background-color: rgb(39, 107, 59);
    margin: 0;
    color: white;
  }
    
</style>
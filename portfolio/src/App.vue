<template>

  <main class="maine">

     <div>   
       
       <div v-show="!mobile" class="desktop">
         <header class="desktoptext">
          <h1 class="desktopheader1">Hello, my name is Samson, also known as Snootnoot</h1>
          <p class ="hobbies">I like to sit in my room all day and procastinate.</p>   
         </header>
         <a href="https://github.com/Snootnoot" target="_blank" rel="noopener noreferrer">
         <img src="./assets/github.png"
         width="60" height="60">
          </a>
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

    .desktopheader1{
      padding-top: 100px;
     
      text-align: center;
      font-size: vmax;
    }

     .hobbies{
    
      text-align: center;
      font-size: 1.3vmax;
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
      top: 0%;
      left: 50%;
      padding-top: 100px;
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
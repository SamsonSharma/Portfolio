<template>
     <div>   
        <ul v-show="!mobile" class="navbar">
            <li>
              <header>
                <h1>
                  {{ title }}
                </h1>
              </header>
            </li>
            <li>
                <div class="button">
                    <Button text="New" class="btn1"/>  
                    <Button text="Best" class="btn2"/>
                    <Button text="Old" class="btn3"/>
                </div>
            </li>
            
        </ul>
     <div v-show="mobile" class="mobilenavbar">
       
          <header class="mobileheader">
            <h1 class="mobiletext">
                {{ title }}
            </h1>
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
</template>

<script>
import Button from './PFContent.vue'
export default {
    name: 'Header',
    props:   {
        title: String,
    },
    components:
    {
        Button,
    },
    data()
    {
      return{
        mobile: true,
        windowWidth: null,
      }
    }
}
</script>
//TODO: add phone switch support to top bar
<style scoped>
  header{
    font-size: 1vw;
    margin: 0px;
    position: absolute;
    top: 50%;
    -ms-transform: translateY(-50%);
    transform: translateY(-50%);
    text-align: left;
    
  }

   .navbar{
    
    position: -webkit-sticky;
    position: sticky;
    list-style-type: none;
    background-color: rgb(39, 107, 59);
    width: 100%;
    max-width: 100%;
    height: 80px;
    border: 0px;
    padding:0px;
    margin:0px;
    top: 0;
    left: 0;

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

    h1{
      
      border: .5px solid rgb(206, 205, 205);
      border-radius: 0 14px 14px 14px;
      padding: 5px;
      margin-left: 1vw;
    }

    .mobiletext{
      border: .5px solid rgb(206, 205, 205);
      border-radius: 0 0px 14px 0px;
      background-color: rgb(39, 107, 59);
      font-size: 5vw;
      margin: 0px;
      width: 45vw;
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
<template>
<section>
<div class="box">
            <div class="form">
                <h2> Login </h2>
                <form method="POST"  action="{{ route('login') }}">
               
                    <div class="inputBox">
                        <label for="">Email</label>
                        <input id="email" type="email" class="form-control" autofocus>
                        <img src="" class="mt-2" alt="">
                     
                        </div> 

                    <div class="inputBox">
                        <label for=""> Password</label>
                        <input id="password" type="password"  class="form-control" name="password" required>
                        <img src="" class="mt-2" alt="">
                       
                    </div>
                    <input class="form-check-input" type="checkbox" name="remember" id="remember" >

                        <label class="form-check-label" for="remember">
                            Remember
                        </label>

                    <div class="inputBox mt-3">
                        <input type="submit" value="Login"> 
                    </div>
                </form>
              
              
            </div>
        </div>
    </section>
</template>


<style>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: sans-serif;
}
section{
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    background: linear-gradient(-30deg , #03a9f4 , #3a78b7 50%,
    #262626 50% , #607d8b 100%);
    /* filter: hue-rotate(120deg); */
    animation: animate 10s linear infinite;
}

@keyframes animate {
    0%{
        filter: hue-rotate(0deg);
    }
    100%{
        filter: hue-rotate(360deg);
    }
}











 .box{
    position: relative;
    padding: 50px;
    width: 360px;
    min-height: 630px;
    display: flex;
    justify-content: center;
    align-items: center;
    background: rgba(255 ,  255, 255, 0.2);
    border-radius: 6px;
    box-shadow: 0 5px 35px rgba(0 ,0 ,0 , 0.2);
}
.box::after{
    content: '';
    position: absolute;
    top: 5px;
    left: 5px;
    right: 5px;
    bottom: 5px;
    border-radius: 5px;
    pointer-events: none;
    background: linear-gradient(to bottom , rgba(255 , 255 , 255 , 0.3) 0% ,
     rgba(255 , 255 , 255 , 0.1) 15% , transparent 50% , transparent 85%,
     rgba(255 , 255 , 255 , 0.3) 100%);
}
.box .form{
    position: relative;
    width: 100%;
}
.box .form h2{
    color: #fff;
    font-weight: 600;
    letter-spacing: 2px;
    margin-bottom: 30px;
}
.box .form .inputBox{
    position: relative;
    width: 100%;
    margin-bottom: 20px;
}
.box .form .inputBox input{
    width: 100%;
    outline: none;
    border: 1px solid rgba(255 ,  255, 255, 0.2);
    background: transparent;
    padding: 8px 10px;
    padding-left: 35px;
    border-radius: 6px;
    color: #fff;
    font-size: 16px;
    font-weight: 300;
    box-shadow: inset 0 0 25px rgba(0 ,0 ,0 , 0.2);
}
.box .form .inputBox input::placeholder{
    color: #fff;
}
.box .form .inputBox input[type="submit"]{
    background: #fff;
    color: #111;
    min-width: 100px;
    padding: 8px 10px;
    box-shadow: none;
    font-weight: 500;
    letter-spacing: 1px;
    cursor: pointer;
}
.box .form .inputBox img{
    width: 22px;
    height: 22px;
    position: absolute;
    top: 25px;
    left: 8px;
    transform: scale(.7);
    filter: invert(1);
}
.remember{
     position: relative;
     display: inline-block;
     color: #fff;
     font-weight: 300;
     margin-bottom: 10px;
     cursor: pointer;
}
.box .form p{
    color: #fff;
    font-weight: 300;
    font-size: 15px;
    margin-top: 5px;
}
.box .form a{
    color: #fff;
}

</style>
<template>
<v-app id="home" :style="{background: $vuetify.theme.themes.dark.background}">

 <MainNavbar />
 

 <v-carousel>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>

  

  
 <div class="row">
  <div class="column" style="background-color:#aaa;">
<div class="row gx-5">
  <div class="col-md-6 mb-4">
    <div class="bg-image hover-overlay ripple shadow-2-strong rounded-5"
      data-mdb-ripple-color="light">
      <img src="https://mdbcdn.b-cdn.net/img/new/slides/080.webp" class="img-fluid" />
      <a href="#!">
        <div class="mask" style="background-color: rgba(251, 251, 251, 0.15);"></div>
      </a>
    </div>
  </div>
    </div>

  <div class="col-md-6 mb-4">
    <h4><span class="badge bg-danger px-2 py-1 shadow-1-strong mb-3">News of the day</span></h4>
    <h4><strong>Enviroment News</strong></h4>
    <p class="text-muted">
     A spokesman from Daera told BBC News NI: "Since going live in 2013, the £37m proceeds of the levy that have been raised have been reinvested to support the wider Northern Ireland environmental sector, everything from birds to bees, water and land, also protecting our countryside and natural heritage..
    </p>
    <button type="button" class="btn btn-primary">Read more</button>
  </div>
</div>


  
   <div class="column" style="background-color:#bbb;">
  <form action="/action_page.php">
  <div class="container">
    <h1>Register</h1>
    <p>Please fill in this form to create an account.</p>
    <hr>

    <label for="email"><b>Email</b></label>
    <input type="text" placeholder="Enter Email" name="email" id="email" required>

    <label for="psw"><b>Password</b></label>
    <input type="password" placeholder="Enter Password" name="psw" id="psw" required>

    <label for="psw-repeat"><b>Repeat Password</b></label>
    <input type="password" placeholder="Repeat Password" name="psw-repeat" id="psw-repeat" required>
    <hr>
    <p>By creating an account you agree to our <a href="#">Terms & Privacy</a>.</p>

    <button type="submit" class="registerbtn">Register</button>
  </div>
  
  <div class="container signin">
    <p>Already have an account? <a href="#">Sign in</a>.</p>
  </div>
</form>
   </div>
   </div> 





  
 <MainFooter />
</v-app>
 
 
</template>

<script>
  import MainNavbar from '../components/MainNavbar'
  import MainFooter from '../components/MainFooter'
 
  export default {
    name: 'HomeView',
    components: {
      MainNavbar,
      MainFooter,
      
    },
data () {
      return {
        items: [
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ],
      }
    },    methods: {
            scroll(refName) {
                const element = document.getElementById(refName);
                element.scrollIntoView({behavior: "smooth"});
            }
      }


      
  }
</script>


<style scoped>
* {
  box-sizing: border-box;
}

/* Create two equal columns that floats next to each other */
.column {
  float: left;
  width: 50%;
  padding: 10px;
  height: 300px; /* Should be removed. Only for demonstration */
}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}


body {
  font-family: Arial, Helvetica, sans-serif;
  background-color: black;
}

* {
  box-sizing: border-box;
}

/* Add padding to containers */
.container {
  padding: 16px;
  background-color: white;
}

/* Full-width input fields */
input[type=text], input[type=password] {
  width: 100%;
  padding: 15px;
  margin: 5px 0 22px 0;
  display: inline-block;
  border: none;
  background: #f1f1f1;
}

input[type=text]:focus, input[type=password]:focus {
  background-color: #ddd;
  outline: none;
}

/* Overwrite default styles of hr */
hr {
  border: 1px solid #f1f1f1;
  margin-bottom: 25px;
}

/* Set a style for the submit button */
.registerbtn {
  background-color: #04AA6D;
  color: white;
  padding: 16px 20px;
  margin: 8px 0;
  border: none;
  cursor: pointer;
  width: 100%;
  opacity: 0.9;
}

.registerbtn:hover {
  opacity: 1;
}

/* Add a blue text color to links */
a {
  color: dodgerblue;
}

/* Set a grey background color and center the text of the "sign in" section */
.signin {
  background-color: #f1f1f1;
  text-align: center;
}























/* carousel */
.media-carousel 
{
  margin-bottom: 0;
  padding: 0 40px 30px 40px;
  margin-top: 30px;
}
/* Previous button  */
.media-carousel .carousel-control.left 
{
  left: -12px;
  background-image: none;
  background: none repeat scroll 0 0 #222222;
  border: 4px solid #FFFFFF;
  border-radius: 23px 23px 23px 23px;
  height: 40px;
  width : 40px;
  margin-top: 30px
}
/* Next button  */
.media-carousel .carousel-control.right 
{
  right: -12px !important;
  background-image: none;
  background: none repeat scroll 0 0 #222222;
  border: 4px solid #FFFFFF;
  border-radius: 23px 23px 23px 23px;
  height: 40px;
  width : 40px;
  margin-top: 30px
}
/* Changes the position of the indicators */
.media-carousel .carousel-indicators 
{
  right: 50%;
  top: auto;
  bottom: 0px;
  margin-right: -19px;
}
/* Changes the colour of the indicators */
.media-carousel .carousel-indicators li 
{
  background: #c0c0c0;
}
.media-carousel .carousel-indicators .active 
{
  background: #333333;
}
.media-carousel img
{
  width: 250px;
  height: 100px
}
/* End carousel */




.top{
  margin-top: 180px;
}  
.topInverse{
  margin-top:  -250px;
}
.topTolbar{
  margin-top: 100px;
  text-align: center;
}
.first{
  width: 100%;
  height: 710px;
  background: linear-gradient(
    to right,
    #181818,
    #181818 50%,
    #111111 50%,
    #111111 50%
  );
  text-align: center;
  padding: 2rem 2rem;
}
.second{
  width: 100%;
  height: 400px;
  background: #181818;
  text-align: center;
  padding: 2rem 2rem;
}
.secondchild1{
  display: inline-block;
  background-color: #1e1e1e;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: left;
  margin-top: 250px;
}
.child{
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: left;
  margin-right: 8px;
}
.bgColor1{
  background-color: #1e1e1e;
}
.bgColor2{
  background-color: #ce1d2a;
}
.child1{
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  margin-right: 5px;
  width: 240px;
}
.child2{
  display: inline-block;
  width: 245px;
  vertical-align: middle;
}
.mRight{
  margin-right: 8px;
}
.mButton{
  margin-bottom: 8px;
}
.padding{
  padding: 12px 0 !important;
}
.col-12 .padd{
  padding: 12px 0 !important;
}
.col-12 .childcol{
  padding: 0 !important;
}
h1.number{
  font-size: 50px;
  font-weight: bold;
}
.wrapper{
  display: flex;
}
.wrapper .static-txt{
  color: #fff;
  font-size: 60px;
  font-weight: 400;
}
.wrapper .dynamic-txts{
  margin-left:  0px;
  height: 90px;
  line-height: 90px;
  overflow: hidden;
}
.dynamic-txts li{
  list-style: none;
  color: #ffffff;
  font-size: 60px;
  font-weight: 500;
  position: relative;
  top: 0;
  animation: slide 12s steps(4) infinite;
}
@keyframes slide {
  100%{
    top: -360px;
  }
}




.dynamic-txts li span{
  position: relative;
  margin: 2px 0;
  line-height: 90px;
}
.dynamic-txts li span::after{
  content: "";
  position: absolute;
  left: 0;
  height: 100%;
  width: 100%;
  background: #111111;
  border-left: 2px solid #ffffff;
  animation: typing 3s steps(10) infinite;
}
@keyframes typing {
  40%, 60%{
    left: calc(100% + 30px);
  }
  100%{
    left: 0;
  }
}




</style>
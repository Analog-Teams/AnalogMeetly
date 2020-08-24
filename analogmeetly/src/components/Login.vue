<template>
<div class="login">
  <div class="header-logo">
    <!-- logo -->
    <img :src="require(`@/assets/${'logo.png'}`)" alt="analogmeetly"><span>Meetly</span>
  </div>
  <!-- login form -->
  <div class="form" :style="{'background-image': 'url('+ require(`@/assets/team.jpg`) + ')'}" style="background-repeat:no-repeat;background-size:cover">
      <h1>Analog Meetly</h1>
    <form class="form-field"> 
      <!-- name -->
      <label for="name">Full Name</label>
      <input type="text" class="form-control" placeholder="Full Name">
      <!-- job number -->
      <label for="job">Job Number</label>
      <input type="text" class="form-control" placeholder="Number">
      <label for="pass">System Password</label>
      <input type="password" class="form-control" placeholder="System Password">
      <input type="submit" value="Login"/>
    </form>
  </div>
  <div class="footer">
    <div class="footer-content">
      <div class="footer-logo">
        <img :src="require(`@/assets/${'flogo.png'}`)" alt="analogteams">
      </div>
      <div class="c1">
        <h4>CONTACT US:</h4>
        <a href="https://twitter.com/analogteams" target="_blank"><i class="fab fa-twitter"><span>Analog on Twitter</span></i></a>
        <a href="mailto:teyibo@analogteams.com" target="_blank"><i class="fas fa-envelope"><span>Email Us</span></i></a>
      </div>
      <div class="c2">
        <h4>LOCATIONS:</h4>
        <i class="fas fa-map-marker-alt"></i>
        <span>Washington D.C., Dallas, Accra, Lagos, Nairobi</span>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: "Login"
}
</script>

<style scoped>
.login{
    max-width:100%;
}
.header-logo {
  width: 100%;
  max-width: 100%;
  height: 20vh;
  background-color:#000;
}
.form{
  width:100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.form h1{
  font-family: 'Poppins', sans-serif;
  position: absolute;
  top:20%;
  color:#fff;
}
.form h1:hover{
  text-decoration: underline;
  transition: 1s ease-in-out;
}
.header-logo span{
  color:#6612ed;
  font-family: 'Poppins', sans-serif;
}
.form-field input[type="submit"] {
  background-color:#fff;
}
.form-field input[type="submit"]:hover{
  background: rgba(255, 255, 255, 0.5);
  transition: 200ms ease-in-out;
}
.footer{
    background-color: #000;
    width: 100%;
    max-width: 100%;
    color: #fff;
}
.footer-content{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}

@media(max-width:768px) {
  .header-logo{
    max-height: 95px;
  }
  .header-logo img{
    max-height: 50px;
    margin:15px;
  }
  .header-logo span{
    font-size: 27px;
    position: absolute;
    top:21px;
    left: 228px;
    text-transform: uppercase;
    font-weight: 900;
    font-family: Arial, Helvetica, sans-serif;
  }
  .form{
    width: 100%;
    max-width: 100%;
    background-position:58%;
  }
  .form h1{
    top:15%;
  }
  .form-field {
    background-color: rgba(10,10,200,0.4);
    border-radius: 10px;
    position: absolute;
    background-attachment: fixed;
    top:25%;
    width: 78%;
    left:12%;
    height: 60vh;
    font-family: 'Poppins',sans-serif;
  }
  .form-field input[type="text"] {
    width: 90%; 
    margin: 2px auto;
  }
  .form-field input[type="password"] {
    width: 90%; 
    margin: 2px auto;
  }
  .form-field input[type="submit"] {
    width: 80%; 
    margin:12px 27px;
    padding: 10px;
    border-radius: 9px;
    outline: none;
    border: none;
    color: #000;

  }
  .form-field label {
    margin: 16px 20px;
    color: #fff;
  }
  .footer-content{
    max-width: 100%;
    height: 40vh;
    display: block;
    margin-left: 20px;
    margin-top:0;
  }
  .footer-content {
    display: flex;
    flex-direction: column;
  }
  .footer-logo {
    margin-left:20px;
  }
  .footer-logo img{
    max-height: 60px;
  }
  .footer-content .c1{
    margin: 10px;
  }
  .footer-content .c1{
    display: flex;
    flex-direction: column;
  }
  .footer-content .c1 i {
    color: #fff;
    margin-top:9px;
  }
  .footer-content .c1 i>span{
      font-family: 'Poppins',sans-serif;
  }
  .footer-content .c2 {
    display: flex;
    flex-direction: column;
    margin-top: 9px;
  }
  .footer-content .c2 i {
    font-size: 20px;
    color:red;
    margin-left:20px;
  }
  .footer-content .c2>span{
    font-family: 'Poppins',sans-serif;
  }
}
@media(min-width:768px) {
  .header-logo{
    max-height: 115px;
  }
  .header-logo img{
    max-height: 95px;
    margin:10px;
  }
  .header-logo span {
     font-family: Arial, Helvetica, sans-serif;
     font-size: 40px;
     position: absolute;
     top:31px;
     left:380px;
     text-transform: uppercase;
     font-weight: 900;
  }
  .form{
    width: 100%;
    max-width: 100%;
    background-position:58%;
  }
  .form-field {
    background-color: rgba(10,10,200,0.4);
    position: absolute;
    border-radius: 20px;
    top:38%;
    width: 50%;
    left:auto;
    height: 50vh;
    font-family: 'Poppins',sans-serif;
  }
  .form-field input[type="text"] {
    width: 50%; 
    margin: 0px auto;
  }
  .form-field input[type="password"] {
    width: 50%; 
    margin: 2px auto;
  }
  .form-field input[type="submit"] {
    width: 20%; 
    margin:2% 39%;
    padding: 10px;
    border-radius: 9px;
    outline: none;
    border: none;

  }
  .form-field label {
    margin: 2.2% 25%;
    color: #fff;
    font-size: 18px;
  }
  .footer-content {
    max-width: 100%;
    height: 24vh;
  }
  .footer-logo{
    margin-left: 280px;
    margin-top: 20px;
  }
  .footer-content .c1{
    margin: 30px 20px;
    display: flex;
    flex-direction: column;
  }
  .footer-content .c2 {
    margin: 30px 400px;
  }
  .footer-content .c1 i{
    color: #fff;
    margin:10px 0px;
  }
  .footer-content .c1 i>span {
  font-family: 'Poppins',sans-serif;
  color:#fff;
  font-size: 20px;
  margin-top: 20px;
  margin-left: 10px;
  }
  .footer-content .c2 i{
    position: absolute;
    left:67%;
    font-size:50px;
    color: red;
  }
  .footer-content .c2 span{
    font-family: 'Poppins',sans-serif;
    font-size: 15.6px;
  }
}

</style>
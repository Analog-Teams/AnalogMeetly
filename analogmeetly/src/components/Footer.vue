<template>
  <div class="footer">
      <div class="logo">
          <img :src="require(`@/assets/${'flogo.png'}`)" alt="analogmeetly">
      </div>
      <div class="location">
          <h2>Location</h2>
          <i class="fas fa-map-marker-alt" style="color:red;"></i><p>Washington D.C., Dallas, Accra, Lagos, Nairobi</p>
      </div>
      <div class="contacts">
          <h2>Contact us</h2>
          <a href="mailto:teyibo@analogteams.com" target="_blank" style="font-family:'Poppins;,sans-serif;"><i class="fas fa-envelope" style="color:#000;"><span>Email Us</span></i></a>
      </div>
  </div>
</template>

<script>
export default {
    name: "Footer"
}
</script>

<style scoped>
    .footer{
        background: rgb(221, 218, 218);  
        font-family: 'Poppins';
    }
    @media(min-width:768px) {
        .footer{
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            height: 20vh;
            max-width: 100%;
            width: 100%;
            margin:30px 20px;
            margin:0;
        }
        .footer img{
            max-width:70px;
        }
        .footer .location{
            margin: 40px;
        }
        .footer .logo{
            margin: 40px 45px;
        }
        .footer .contacts{
            margin: 40px;
        }
        .footer .location i{
            font-size: 30px;
            position: absolute;
            left: 34%;
        }
    }
    /* smaller devices */
    @media(max-width:768px) {
        .footer{
            display: block;
            margin: -10px 0;
            max-width: 100%;
            width: 100%;
            height: 45vh;
        }
        .footer .logo{
            margin: 20px 18px;
        }
        .footer .logo img{
            margin-top: 14px;
            max-width: 50px;
        }
        .footer .location h2{
            font-size: 20px;
        }
        .footer .location p{
            font-size: 12px;
        }
        .footer .location{
            margin:10px;
        }
        .footer .contacts h2{
            font-size: 20px;
        }
        .footer .contacts p{
            font-size: 12px;
        }
        .footer .contacts {
            margin: 10px;
        }
        .footer .location i{
            font-size: 30px;
        }
    }
    
</style>
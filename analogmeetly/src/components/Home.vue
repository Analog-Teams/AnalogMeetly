<template>
      <div class="home">
          <!-- navbar -->
        <nav class="navbar navbar-expand-lg" id="nav">
        <img :src="require(`@/assets/${'logo.png'}`)" alt="analog"><span id="span">meetly</span>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon">___</span><br />
            <span class="navbar-toggler-icon">___</span><br />
            <span class="navbar-toggler-icon">___</span><br />
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
            <li class="nav-item active">
                <a class="nav-link" href="#">Home<span class="sr-only">(current)</span></a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="#">Features</a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="#" tabindex="-1" aria-disabled="true">Logout</a>
            </li>
            </ul>
        </div>
        </nav>
        <div class="about">
            <!-- about-img -->
            <div class="about-img">
                <img :src="require(`@/assets/${'ab3.png'}`)" alt="about">
            </div>
            <!-- description -->
            <div class="desc">
                <h1>Home</h1>
                <p><strong>AnalogMeetly</strong> is a web-based system,that can be used to record meeting notes,organize meeting notes,
                    search meeting based on date,time,type or search meeting notes using the same criteria.
                </p>
            </div>
        </div>
      </div>
</template>

<script>
export default {
    name: "Home"
}
</script>

<style scoped>
    #nav{
        max-width: 100%;
        background:#000;
    }
    .nav-item .nav-link{
        color:#fff;
        font-family: 'Poppins',sans-serif;
    }
    .about{
       max-width: 100%;
    }
    /* smaller devices */
    @media (max-width:768px) {
        #nav{
            max-width: 100%;
            padding: 25px;
        }
        #nav img{
            max-height: 45px;
            margin-left: -10px;
        }
        #nav #span{
            color: #6613ED;
            font-family: 'Poppins',sans-serif;
            font-size: 25px;
            text-transform: uppercase;
            position: absolute;
            left:183px;
            top:42px;
        }
        .home button > span{
            display: block;
            max-height:0.1px;
            color:#fff;
            position: absolute;
            left:310px;
        }
        .home button{
            outline: none;
        }
        .about{
            display:flex;
            flex-direction: column;
            background:rgb(144, 145, 202);
            height: 90vh;
        }
        .about .desc{
            position: absolute;
            top:40%;
        } 
        .about-img {
            max-width: 100%;
            width: 100%;
        }
        .about-img img{
            max-height:45%;
            position: absolute;
            top:20%;
            left:-10%;
        }
        .about .desc h1{
           position: absolute;
           top:30%;
           left:4%;
           font-size: 40px;
        }
        .about .desc p{
            font-family: sans-serif;
            font-weight: 400;
            font-size: 17.5px;
            margin:290px 12px;
        }
    }
    /* large screens */
    @media (min-width:768px) {
        #nav{
            max-width: 100%;
            padding: 35px;
        }
        .nav-item .nav-link {
            font-size: 20px;
        }
        #nav img{
            max-height: 75px;
        }
         #nav #span{
            color: #6613ED;
            font-family: 'Poppins',sans-serif;
            font-size: 35px;
            text-transform: uppercase;
            position: absolute;
            left:318px;
            top:50px;
        }
        .navbar-nav{
            position: absolute;
            left:75%;
        }
        .nav-item .nav-link{
            margin-left:30px;
        }
        .nav-item .nav-link:hover {
            text-decoration: underline;
            color: #6613ED;
            transition: 500ms ease-in;
        }
        .about{
            display: grid;
            grid-template-columns: 1fr 1fr;
            max-width: 100%;
            width: 100%;
            height: 90vh;
            max-height: 100%;
            background:rgba(0,0,250,.38);
            color: #000;
        }
        .about .about-img{
            position: absolute;
            top:13%;
        }
        .about .about-img img{
            max-width:70%;
            height: auto;
        }
        .about .desc{
            position: absolute;
            left:60%;
            top:25%;
            right: 4%;
        }
        .about .desc p{
            font-family: 'Poppins',sans-serif;
            font-weight: 500;
            line-height: 1.7em;
        }
    }
</style>
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
                <a class="nav-link" href=".home">Home<span class="sr-only">(current)</span></a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href=".features">Features</a>
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
                <p><strong>AnalogMeetly</strong> is a web application that can be used to record meeting notes,organize meeting notes,
                    search meeting based on date,time,type or search meeting notes using the same criteria.
                </p>
                <button type="button" @click="readMore">Read More</button>
            </div>
        </div>
        <!-- features -->
        <div class="features">
            <div class="card-group">
                <div class="card">
                    <img :src="require(`@/assets/${'a.jpg'}`)" alt="features" style="max-width:100%;height:auto">
                    <div class="card-body">
                    <h5 class="card-title">Add Meeting Note(s)</h5>
                    <p class="card-text">One of the biggest struggles people have with note-taking is keeping their notes organized in a way that they can actually find and revisit in a valuable way later.AnalogMeetly provides a one-time solution by keeping notes neat and well organized.</p>
                    <p class="card-text"><small class="text-muted">{{timer}}</small></p>
                    </div>
                </div>
                <div class="card">
                     <img :src="require(`@/assets/${'d.jpg'}`)" alt="features" style="max-width:100%;height:auto">
                    <div class="card-body">
                    <h5 class="card-title">Search Meeting(s)</h5>
                    <p class="card-text">AnalogMeetly provides a systematic way to seacrh meetings based on time,the type of meeting,attendants and so on.With AnalogMeetly,you can get access to the past meetings,what was discussed,the type of meeting and even those who attended.</p>
                    <p class="card-text"><small class="text-muted">{{timer}}</small></p>
                    </div>
                </div>
                <div class="card">
                    <img :src="require(`@/assets/${'h.jpg'}`)" alt="features" style="max-width:100%;height:auto">
                    <div class="card-body">
                    <h5 class="card-title">Search Meeting Note(s)</h5>
                    <p class="card-text">One of the main objectives of AnalogMeetly is to provide a systematic access to meeting record.It filters meeting notes according to the specified criteria.This ensures that the right record is retrived in an organized manner.</p>
                    <p class="card-text"><small class="text-muted">{{timer}}</small></p>
                    </div>
                </div>
            </div>
        </div>
      </div>
</template>

<script>
export default {
    name: "Home",
    computed: {
        timer() {
            return new Date().toString()
        }
    },
    methods: {
        readMore() {
            return window.location = 'https://analogteams.com'
        }
    }
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
            color:#9875d6;
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
            display:block;
            max-width: 100%;
            background: #cbc4d6;
        }
        .about .about-img{
            max-width: 100%;
        }
        .about .about-img img{
            max-width: 100%;
            height: auto;
        }
        .about .desc{
            margin:20px;
            max-width: 100%;
        }
        .about .desc h1{
            font-family: 'Poppins',sans-serif;
            font-size: 40px;
        }
        .about .desc p{
            margin-top:25px;
            font-family:sans-serif;
            font-size: 17px;
        }
        .about .desc button{
            padding: 20px;
            width: 65%;
            max-width: 70%;
            border: none;
            background: #7b49cc;
            color:#fff;
            font-family: 'Poppins',sans-serif;
            font-size: 20px;
            margin-top:40px;
            margin-bottom: 30px;
            cursor: pointer;
        }
         .features .card-title{
            font-family: 'Poppins';
        }
        .features .card-text{
             font-family: 'Baloo Tamma 2', cursive;
             font-size: 18px;
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
            height: 70vh;
            max-height: 70vh;
            background:rgba(0,0,250,.38);
            color: #000;
        }
        .about .about-img{
            position: absolute;
            top:8%;
        }
        .about .about-img img{
            max-width:60%;
            height: auto;
        }
        .about .desc{
            position: absolute;
            left:56%;
            top:18%;
            right: 4%;
        }
        .about .desc h1{
            font-size: 50px;
            font-family: 'Poppins',sans-serif;
        }
        .about .desc p{
            font-family: 'Baloo Tamma 2', cursive;
            line-height: 1.7em;
            font-weight: 500;
            font-size: 22px;
        }
        .about .desc button{
            padding: 20px;
            width: 40%;
            max-width: 70%;
            border: none;
            background:#6613ED;
            color:#fff;
            font-family: 'Poppins',sans-serif;
            font-size: 20px;
            margin-top:40px;
            margin-bottom: 30px;
            cursor: pointer;
            outline: none;
            transition: 300ms ease-in-out;
        }
        .about .desc button:hover{
            transform: scale(1.09);
            text-decoration: underline;
        }
        .features{
            margin-top:2%;
        }
        .features .card-title{
            font-family: 'Poppins';
            font-size: 26px;
        }
        .features .card-text{
             font-family: 'Baloo Tamma 2', cursive;
             font-size: 20px;
        }
    }
</style>
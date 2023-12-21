


<div id = "about" class="about">
    <div class="title">
        <h1>About Me</h1>
    </div>

    <div class="container">
        <div class="picture">
            <img src="/images/bananastand.png" alt="">
        </div>

        <div class="description">
            <h3>I am an Army veteran currently in my last year of pursuing my bachelors in computer science. 
            I am originally from Florida and enlisted in the Army after graduating high school. I've had three internships,
            one at Amazon Web Services, the Securites and Exchange Commission, and the Naval Air Warfare Center Weapons Division,
            as well as an academic experience with NASA. In my free time I enjoy jiu jitsu and playing chess.
            </h3>
        </div>

    </div>
</div>
<div class="spacer"></div>

<style>
    .spacer{
        height: 15vh;
    }
    .about{
        font-family: "Open Sans",sans-serif;
        max-width: 1600px;
        margin:auto;
    }
    .title{
        text-align: center;
        color: #bae8e8;
        margin:auto;
    }
    .container{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        border-style:solid;
        border-radius: 5px;
        padding: 30px 10px 10px 10px;
        box-shadow: 0px 0px 15px #fbfbfb inset;   
        
    }
    .description{
        max-width: 40em;
    }
    h1{
        font-size: 60px;
    }
    h3{
        text-align: center;
        font-size: 20px;
        color: #bae8e8;
    }
    img{
        width: 400px;
        height: 400px;
        object-fit: cover;
        border-radius: 20px;
        box-shadow: 0px 0px 10px #8dc6ff;
        transition: .5s;
    }

    img:hover{
        padding: 2px 2px;
        box-shadow: 0px 0px 20px #8dc6ff;
    }

</style>
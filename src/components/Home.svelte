<script>
    import {fade, fly} from 'svelte/transition';
    import {tweened} from 'svelte/motion';
    let titles = ['Software Engineer', 'Incoming SDE @ AWS', 'Army Veteran', 'Student']
    let titleIndex = 0; 
    let title = titles[titleIndex];
    
    const switchTitle = () => {
        if(titleIndex == 3){
            titleIndex = 0;
        }else{
            titleIndex = titleIndex + 1;
        }
        title = titles[titleIndex];
        
    }
    setInterval(switchTitle, 3000, titleIndex);

    const scrollToAbout = () => {
        scrollTo(0, 1000);
   }

</script>

<div class="home">
    <div class="intro">
        <h1>
            {#if titleIndex == 0 || titleIndex == 3}
                <h1 class = 'title'> I'm a {title} </h1> 
            {:else}
                <h1 class = 'title'>I'm an {title}</h1>
            {/if}  
        </h1>
         
        <h3> Interested in developing and implementing efficient solutions to real world problems.</h3>
        <h3><a class = 'continue' href = "" on:click = {scrollToAbout}>Learn More</a></h3>
    </div>
    
    <div class="codeScroll">
        <!-- svelte-ignore a11y-media-has-caption -->
        <video autoplay = true loop = true id = 'video' class = 'codeScroll'  >
            <source src = "/images/CodeScrolling.mp4" type = 'video/mp4'>
        </video>
    </div>
</div>




<style>
    .home{
        color: #bae8e8;
        display: flex;
        margin-bottom: 40%;
        margin-top: 10%;
        font-family: "Open Sans",sans-serif;
        }
    .intro{
        max-width: 50em;
        margin-top:20px
    }
    .codeScroll{
        display:flex;
        margin:auto;
    }
    
    video{
        max-height: 1500px;
        max-width: 1500px;
        height:65%;
        width:65%;
        border-radius: 20px;
        box-shadow: 0px 0px 20px #8dc6ff;
        transition: .5s;
    }
    video:hover{
        padding: 7px 7px;
        box-shadow: 0px 0px 40px #8dc6ff;
    }
    h1{
        text-align: center;
        font-size: 60px;
    }
    h3{
        text-align: center;
        margin-bottom: 50px;
        font-size: 20px;
        color: #8dc6ff;
    }
    .continue{
        margin-top: 50px;
        font-size: 20px;
        color: #8dc6ff;
        text-decoration: none;
        transition: .5s;
        border-style:solid;
        border-radius: 5px;
        padding: 10px 10px;
        box-shadow: 0px 0px 10px #8dc6ff;
    }

    .continue:hover{
        padding: 15px 15px;
        box-shadow: 0px 0px 20px #8dc6ff;
        color:white;
    }
    
</style>
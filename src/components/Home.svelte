<script>
    import {fade, fly} from 'svelte/transition';
    import {tweened} from 'svelte/motion';
    import { animateScroll } from 'svelte-scrollto-element';
    let titles = ['Software Engineer', 'SDE Intern @ AWS', 'Army Veteran', 'Student']
    let titleIndex = 0; 
    let title = titles[titleIndex];
    let borderBound = 10;
    let increase = true;
    
    const switchTitle = () => {
        if(titleIndex == 3){
            titleIndex = 0;
        }else{
            titleIndex = titleIndex + 1;
        }
        title = titles[titleIndex];
        
    }
    setInterval(switchTitle, 3000, titleIndex);
    
   const changeBorder = () => {
    if(borderBound == 45)
        increase = false;
    else if(borderBound == 10)
        increase = true;

    if(increase)
        borderBound += 1;
    else
        borderBound -= 1;
   }
   setInterval(changeBorder, 100, borderBound);

</script>
<div class = "home-before"></div>

<div class="home" style = "--box-shadow: {borderBound.toString() + 'px'};">
    <div class="intro">
        <h1 class = 'title'> {title} </h1> 
         
        <h3> Interested in developing and implementing efficient solutions to real world problems.</h3>
        <h3><a class = 'continue' href = "" on:click = {() => animateScroll.scrollToTop({offset: 500})}>Learn More</a></h3>
    </div>
</div>
<div class = "home-before"></div>

<style>
    .home{
        color: #bae8e8;
        display: flex;
        font-family: "Open Sans",sans-serif;
        border-style: solid;
        border-radius: 100px;
        width: fit-content;
        margin:auto;
        padding: 10px 0px 10px 20px;
        box-shadow: 0 0 var(--box-shadow) #8dc6ff;
        transition: .1s smooth;
    }
    .home-before{
        height: 15vh;
    }
    .intro{
        max-width: 50em;
        margin-top:20px;
        margin:auto;
    }

    h1{
        text-align: center;
        min-height: 140px;
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

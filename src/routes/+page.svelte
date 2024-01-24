<script>
    /*ToDo
        *Caption 
    */

    import Header from '../components/Header.svelte';
    import Page1 from '../components/Page1.svelte';
    import Home from '../components/Home.svelte';
    import Footer from '../components/Footer.svelte';
    import About from '../components/About.svelte';
    import Sidebars from '../components/Sidebars.svelte';
    import Projects from '../components/Projects.svelte';
    import { fade } from 'svelte/transition';
    import { element } from 'svelte/internal';

    let arr = [1,2,3];
    let color = 0;
    let count = 0;
    let visible = true;

    let min = 10;
    let mid = 10;
    let max = 253; 

    const stopPreload = () => {
        clearInterval(myinterval);
        visible = false;
    }

    //Change gradient colors 
    const colorChange = () => {
        if(count == 50){
            if(color == 2)
                color = 0;
            else
                color++;
        }

        if(color == 0)
            min++;
        if(color == 1)
            mid++;
        if(color == 2)
            max--;
        
        count++;
    }

    //Call for color change 
    let myinterval = setInterval(colorChange, 10);

    //Call for stoppage of colorChange and remove preloader
    setTimeout(stopPreload, 2000);

</script>

<body>
    
    <!-- {#if visible == true}
        <div id = 'preloader' out:fade = "{{duration: 1000}}" style = "--max-color: {min}; --mid-color: {mid}; --min-color: {max}; " class="preloader">
            Cody Cole 
        </div>
    {/if} -->
    <Header/>
    <Home/>
    <Sidebars/>
    <About/>
    <Projects/>
    <Footer/>
</body>

<style>
body{
    background-color: #240747;
    background-image: linear-gradient(to left, #240747, #3e1c68);
}

.preloader{
    color: white;
    font-size: 60px;
    display: flex;
    position: fixed;
    height: 100vh;
    width: 100%;
    left: 0;
    top: 0;
    z-index: 2;
    justify-content: center;
    align-items: center;
    background: rgb(131,58,180);
    background: linear-gradient(90deg, rgba(131,58,180,1) 1%, rgba(var(--max-color),var(--mid-color),var(--min-color),1) 100%);
}
</style>

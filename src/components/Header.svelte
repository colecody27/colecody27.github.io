<script>
    import { animateScroll } from 'svelte-scrollto-element';
    function scrollIntoView({ target }) {
        const el = document.querySelector(target.getAttribute('href'));
        if (!el) return;
        el.scrollIntoView({behavior: 'smooth'});
    }
</script>

<div class="header">
    <div class="name"> CC </div>
    <div class = "navbar">
        <ul class = "navbarLinks">
            <li id = 'about'><a href = "#about" on:click = {() => animateScroll.scrollToTop({offset: 500})} > About</a></li>
            <li id = 'projects'><a href = "#projects" on:click = {() => animateScroll.scrollToTop({offset: 2000})}> Projects</a></li>
            <li id = 'connect'><a href = "#contact" on:click = {() => animateScroll.scrollToBottom()}> Contact</a></li>
            <li class = 'resume'><a href="https://drive.google.com/file/d/19zoxScu72WodWbRySdFJUgOCloFwLYX0/view?usp=sharing">Resume</a></li>
        </ul>
    </div>
</div>

<style>
    .header{
        display: flex;
        justify-content: space-between;
        width: 98%;
        font-family: "Open Sans",sans-serif;
        font-size: 25px ;
        font-weight: bolder;
        color: #8dc6ff;
        position:fixed;
        top: 0;
        background-color: #240747;
        background-image: linear-gradient(to left, #240747, #3e1c68);
        z-index: 1;
    }
    .name{
        transition: .5s;
        border-style:solid;
        border-radius: 70px;
        padding: 20px 20px 20px 20px;
        box-shadow: 0px 0px 10px #8dc6ff;
    }

    .name:hover{
        box-shadow: 0px 0px 20px #8dc6ff;
        transition: .7s;
    }

    .navbar{
        display: flex;
    }
    .navbar li{
        list-style: none;
        display: inline;
        margin-bottom: 5px;
    }
    .navbarLinks li a:hover{
        color: #ffffff;
        transition: .5s;
    }
    .navbar li a{
        text-decoration-line: none;
        margin-right: 20px;
        color: inherit;
    }
    .resume{
        transition: .5s;
        border-style:solid;
        border-radius: 5px;
        padding: 10px 0px 10px 20px;
        box-shadow: 0px 0px 10px #8dc6ff;
    }
    .resume:hover{
        padding: 20px 10px 20px 30px;
    }
</style>


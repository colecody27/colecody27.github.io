<script>
    let myStats = [
        ['Languages', 'Java', 'javascript', 'R',],
        ['Internships', 'Incoming SWD @ AWS', 'S.E.C', 'NAWCWD']
    ]
</script>
<body>
    <div class = 'video'>
        <!-- svelte-ignore a11y-media-has-caption -->
        <video autoplay = true loop = false id = 'video' class = 'codeScroll' >
            <source src = "/images/CodeScrolling.mp4" type = 'video/mp4'>
        </video>
    </div>

    <div class="stats">
        <ul class = statList>
            <li>{myStats[0][0]} : Incoming SDE @ AWS</li>
            <li>Internships: 3 </li>
            <li>Graduation: Spring 2024</li>
            <li>Primary Language: Java </li>
            <li>Currently learning: Something</li>
        </ul>
    </div>

</body>

<style>
    body{
        background-color: #808080;
        height: 80vh;
        box-shadow: 0px 0px 20px #808080;
        display: flex;
    }

    .codeScroll{
        height: 100%;
        width: 100%;
    }
    .stats{
        color: white;
        margin: auto;
        font-size: 35px;
        font-family: Georgia, 'Times New Roman', Times, serif;
        
    }
    .statList li{
        list-style: none;
        margin-top: 40px;
    }
</style>
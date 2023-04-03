<div class = projectSection>
    <!--Headline-->
    <div class="title">
        <h1>Projects</h1>
    </div>

    <!--Projects-->
    <div class="projects">
        <div class="project">
            <a href="https://github.com/colecody27/CCole_SortComparison_F20">
                <h3 class = 'title'>Sort Comparison<img class = "github" src="/images/github.png" alt=""></h3>
                <h4 class = 'description'>
                    Three self developed sorting algorithms: insertion, quick, and merge sort. 
                </h4>
                <ul class = 'skills'>
                    <li>Java</li>
                    <li>Time & Space Complexity</li>
                    <li>Data Structures</li>
                </ul>
            </a>
        </div>
        <div class="project">
            <a href="https://github.com/colecody27/Lexical_Analyser">
                <h3 class = 'title'>Lexical Analyser<img class = "github" src="/images/github.png" alt=""></h3>
                <h4 class = 'description'>
                    Receives a list of tokens in a string and outputs the list of lexemes.
                </h4>
                <ul class = 'skills'>
                    <li>Java</li>
                    <li>Parsers</li>
                    <li>Compilers</li>
                </ul>
            </a>
        </div>
        <div class="project">
            <a href="https://github.com/colecody27/Data_Structs">
                <h3 class = 'title'>DS Visualizer<img class = "github" src="/images/github.png" alt=""></h3>
                <h4 class = 'description'>
                    Website that visualizes the functionality of data structures: Linked list and Stacks. 
                </h4>
                <ul class = 'skills'>
                    <li>Javascript</li>
                    <li>HTML & CSS</li>
                    <li>Data Structures</li>
                </ul>
            </a>
        </div>
        <div class="project">
            <a href="https://github.com/Saul385/CtrlHabits.com">
                <h3 class = 'title'>CtrlHabits.com<img class = "github" src="/images/github.png" alt=""></h3>
                <h4 class = 'description'>
                    A web application that merges social media and productivity
                    enabling users to connect and observe the progress of their goals and friends.
                </h4>
                <ul class = 'skills'>
                    <li>Sveltekit</li>
                    <li>Firebase</li>
                    <li>Web Design</li>
                </ul>
            </a>
        </div>
        <div class="project">
            <a href="https://github.com/colecody27/CCole_SpellChecker_F20">
                <h3 class = 'title'>Spell Checker<img class = "github" src="/images/github.png" alt=""></h3>
                <h4 class = 'description'>
                    A web application that merges social media and productivity
                    enabling users to connect and observe the progress of their goals and friends.
                </h4>
                <ul class = 'skills'>
                    <li>Java</li>
                    <li>BSTs</li>
                    <li>Time & Space Complexity</li>
                </ul>
            </a>
        </div>
        <div class="project">
            <a href="https://github.com/colecody27/CCole_XmlValidator_F20">
                <h3 class = 'title'>XML Validator<img class = "github" src="/images/github.png" alt=""></h3>
                <h4 class = 'description'>
                    Uses an XmlTagStack to validate the nesting of XML elements in xmlDocument.
                </h4>
                <ul class = 'skills'>
                    <li>Java</li>
                    <li>Stacks</li>
                    <li>Regex</li>
                </ul>
            </a>
        </div>
    </div>
   
</div>

<style>
    .projectSection{
        margin-bottom: 20%;
        
    }
    .projects{
        max-width: 1000px;
        margin-left: 20px;
        margin:auto;
        display: flex;
        flex-wrap: wrap;
    }
    .title{
        text-align: center;
        color: #bae8e8;
        margin:auto;
    }
    h1{
        font-size: 60px;

    }
    .project{
        background-color: #222831;
        height: 200px;
        width: 250px;
        margin: auto;
        margin-bottom: 30px;
        transition: .5s;
        border-style:solid;
        border-radius: 5px;
        padding: 10px 10px 10px 10px;
        box-shadow: 0px 0px 10px #8dc6ff;   
    }
    .project:hover{
        padding: 15px 15px 15px 15px;
        box-shadow: 0px 0px 20px #8dc6ff; 
    }
    .title{

        font-size: 20px;
    }
    .description{
        color: #8dc6ff;
        height: 60px;
    }
    .project a{
        text-decoration: none;
    }

    .github{
        height: 40px;
        width: 40px;
        margin-left: 40px;
        border-radius: 100px;
        filter: invert(100%);
        transition: .5s;
    }
    .github:hover{
        height: 55px;
        width: 55px;
        filter: invert(0%);
    }
    .skills{
        list-style: none;
        text-decoration: none;
        display: flex;
        padding-left: 0;
    }
    .skills li{
        margin-right: 20px;
        color: #bae8e8;
    }

</style>
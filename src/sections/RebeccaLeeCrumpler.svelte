<script>
import Scroller from "../lib/Scroller.svelte";
import ArticleText from "../lib/ArticleText.svelte";
</script>
<div id="title">
    <h1>
        Dr. Rebecca Lee Crumpler
    </h1>
</div>
<div>
    <div class="scrolling">
    <Scroller layout="right">
        {#snippet sticky()}
            <div class="box">
                <img id="picture" src="rebecca-lee-crumpler.jpeg" alt="crumpler">
            </div>
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                In 1864, Rebecca Lee Crumpler became the first Black female doctor in the United States. 
            </ArticleText>

            <ArticleText>
               Not only was she the first Black female doctor; she was the first African American woman to graduate from college. 
            </ArticleText>

            <ArticleText>
                After graduating from New England Female Medical College, the first all-female medical school in the US, 
                Crumpler worked with the Freedmen’s Bureau and missionary groups with a goal in helping emancipated slaves 
                in need of medical care in Richmond.<sup>6</sup>

            </ArticleText>

            <ArticleText>
                Crumpler wrote A Book of Medical Discourses in 1883, which is believed to be one of the first medical books written by an African American.<sup>6</sup>

            </ArticleText>
            <ArticleText>
              Read more about Rebecca Lee Crumpler
                <a href="https://www.womenshistory.org/education-resources/biographies/rebecca-lee-crumpler" target="_blank" >here</a>.
            </ArticleText>


        {/snippet}
    </Scroller>
    </div>
</div>

<style>
    #picture {
        padding: 0px;
        width: 700px;
        overflow: auto;
        align-items: left;
    }
     .box {
        vertical-align: top;
        text-align: left;
    }
     .scrolling{
       height: 5500px;
       background-color: black;
    }
    a{
        color: white;
    }
    #title{
        align-items: right;
        background-color: #000000;
        color: white;
        font: 'Georgia';
        margin: 0px;
        padding: 2%;
        height: 0px;
        vertical-align: right;
        font-size: large;
    }
    h1{
        text-align: right;
        vertical-align: bottom;
        margin-top: 20%;
        font-size: 50px;
    }
</style>

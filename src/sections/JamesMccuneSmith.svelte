<script>
import Scroller from "../lib/Scroller.svelte";
import ArticleText from "../lib/ArticleText.svelte";
</script>
<div id="title">
    <h1>
        Dr. James McCune Smith
    </h1>
</div>
<div>
    <div class="scrolling">
    <Scroller layout="left">
        {#snippet sticky()}
            <div class="box">
                <img id="picture" src="james-mccune-smith.jpg" alt="smith">
            </div>
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                In 1837, James McCune Smith became the first Black doctor in the United States. 
            </ArticleText>

            <ArticleText>
               Smith was <strong>denied entry</strong> to several US colleges when he was in pursuit of his medical degree.
            </ArticleText>

            <ArticleText>
                He had to study at the University of Glasgow in Scotland, 3258.629 miles away from New York City.

            </ArticleText>

            <ArticleText>
               After completing his education in Glasgow, Smith interned in Paris and moved back to New York City, 
               opening a pharmacy that served patients of any race. Smith was an abolitionist who advocated 
               to end slavery, promoted education for black youth, protected runaway slaves, and countless
                other actions that protested racism.<sup>5</sup>
            </ArticleText>
            <ArticleText>
               In 1855, Smith co-founded the interracial Radical Abolitionist Party, with Frederick Douglass,
                former Congressman Gerrit Smith, and John Brown.<sup>5</sup>
            </ArticleText>
            <ArticleText>
              Read more about James McCune Smith
                <a href="https://www.smithsonianmag.com/history/james-mccune-smith-america-first-black-physician-180977110/" target="_blank" >here</a>.

            </ArticleText>


        {/snippet}
    </Scroller>
    </div>
</div>

<style>
    #picture {
        padding: 0px;
        height: 800px;
        overflow: auto;
        align-items: center;
    }
     .box {
        vertical-align: top;
        text-align: center;
    }
     .scrolling{
       height: 6750px;
       background-color: black;
    }
    a{
        color: white;
    }
    #title{
        align-items: center;
        background-color: #000000;
        color: white;
        font: 'Georgia';
        margin: 0px;
        padding: 5%;
        height: 100px;
        vertical-align: bottom;
        font-size: large;
    }
    h1{
        vertical-align: bottom;
        margin-top: 20%;
        font-size: 50px;
    }
</style>

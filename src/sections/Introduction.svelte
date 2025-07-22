<script>
import Scroller from "../lib/Scroller.svelte";
import ArticleText from "../lib/ArticleText.svelte";
</script>

<div>
    <div class="scrolling">
    <Scroller layout="right">
        {#snippet sticky()}
            <div class="box">
                <img id="picture" src="intro_image2.png" alt="doctorpatient">
                
            </div>
            <p>Image Source: <a href="https://abcnews.go.com/GMA/Wellness/new-race-neutral-kidney-evaluation-moves-thousands-black/story?id=109039615" target="_blank"> ABC News</a></p>

        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                55% of Black adults report that they’ve had at least one negative experience 
                with health care providers in the past, such as feeling they had to speak up 
                to get the proper care or that the pain they were experiencing was not being 
                <strong>taken seriously</strong>.<sup>1</sup>
            </ArticleText>

            <ArticleText>
               Studies show that patients assigned to a Black doctor are more likely 
               to demand preventive health care services.<sup>2</sup>

            </ArticleText>
            <ArticleText>
                Research shows that <strong>Black healthcare representation</strong> is 
                associated with higher life expectancy by 30.61 days for all individuals.<sup>3</sup>

            </ArticleText>

            <ArticleText>
               They also found that higher Black representation was associated with smaller 
               mortality differences between Black and White individuals.<sup>3</sup>
            </ArticleText>



        {/snippet}
    </Scroller>
    </div>
</div>

<style>
    #picture {
        padding: -10px;
        width: 100%;
        overflow: auto;
        align-items: center;
    }
     .box {
        vertical-align: top;
        text-align: center;
    }
     .scrolling{
       height: 4700px;
       background-color: black;
    }
    p{
        color: white;
        
    }
    a{
        color: white;
    }
</style>

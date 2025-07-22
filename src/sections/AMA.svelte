<script>
import Scroller from "../lib/Scroller.svelte";
import ArticleText from "../lib/ArticleText.svelte";
</script>

<div>
    <div class="scrolling">
    <Scroller layout="right">
        {#snippet sticky()}
            <div class="box">
                <img id="picture" src="AMA.png" alt="ama">
            </div>
            <p>Image Source: <a href="https://www.rebelnews.com/american_medical_association_language_critical_race_theory" target="_blank">Rebel News</a></p>
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
            The American Medical Association (AMA) was founded in 1847 by White males, 
            more than a third of whom came from slaveholding or border states.            
            </ArticleText>
            <ArticleText>
               From the beginning, it was known that the AMA saw Black Americans as a threat to their goal of 
               raising the prestige and pay for American physicians.<sup>10</sup>
            </ArticleText>

            <ArticleText>
                After 1870, the AMA passed laws that require physicians to pass a test, meet educational requirements, 
                and complete an internship to practice medicine.<sup>10</sup>
            </ArticleText>

            <ArticleText>
                The organization also required membership in a local medical society to join, 
                and almost all local societies barred Black members, except the Washington DC chapter.<sup>10</sup>
            </ArticleText>

            <ArticleText>
                In 1904, the AMA hired Abraham Flexner to study the standards of US and Canadian medical schools. 
                Flexner declared that Black doctors were only needed to keep contagious diseases away from 
                White people.<sup>10</sup>
            </ArticleText>

            <ArticleText>
                Because of this, he recommended closing multiple historically Black medical schools, claiming that 
                “The negro needs good schools, rather than many schools.”
            </ArticleText>

            <ArticleText>
                At the time there were seven historically Black medical schools.
            </ArticleText>

            <ArticleText>
              By 1924, there were only <strong>two left</strong>.
            </ArticleText>

            <ArticleText>
             Due to the strong restrictions, inaccess to local AMA chapters, and lack of medical schools, it became incredibly difficult to become a doctor as a Black American.
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
        align-items: center;
    }
     .box {
        vertical-align: top;
        text-align: center;
    }
     .scrolling{
       height: 9500px;
       background-color: black;
    }
    a{
        color: white;
    }
     p{
        color: white;
        
    }
    a{
        color: white;
    }
</style>

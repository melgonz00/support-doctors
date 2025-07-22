<script>
import Scroller from "../lib/Scroller.svelte";
import ArticleText from "../lib/ArticleText.svelte";
</script>
<div id="title">
    <h1>
        Dr. Rebecca J. Cole
    </h1>
</div>
<div>
    <div class="scrolling">
    <Scroller layout="left">
        {#snippet sticky()}
            <div class="box">
                <img id="picture" src="rebecca-j-cole.jpeg" alt="cole">
            </div>
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                Soon after Rebecca Lee Crumpler, Rebecca Lee Cole became the second Black female doctor in the US in 1864.  
            </ArticleText>

            <ArticleText>
               Cole also attended New England Female Medical School, and wrote a thesis called "The Eye and Its Appendages."<sup>7</sup>
            </ArticleText>

            <ArticleText>
                Cole was an advocate for the poor and public health. 
                She frequently visited poor mothers to inform them on caring for infants and preserving the health of their families.<sup>7</sup>
            </ArticleText>

            <ArticleText>
                In 1873, Cole opened a Women's Directory Center to provide medical and legal services to destitute women and children in Philadelphia.<sup>7</sup>
            </ArticleText>
              <ArticleText> Cole is known for her well-publicized dispute with activist and scholar, W.E.B. Dubois.
            Tuberculosis was more prevalent after the emancipation of slavery and
            Dubois blamed this on Black Americans’ ignorance of proper hygiene. Cole countered this,
            explaining that the discriminatory practices of white doctors prevent Black people from being properly treated.<sup>8</sup>
            </ArticleText>
            <ArticleText>“[H]osts of the poor are attended by young, inexperienced white physicians,” she wrote in response to DuBois 
                in the periodical The Women’s Era. “They inherited the traditions of their elders, and let a black patient cough, 
                they immediately have visions of tubercles... he writes ‘tubercolosis’ [sic] and heaves a great sigh of relief 
                that one more source of contagion is removed.”<sup>8</sup>
            </ArticleText>
            <ArticleText>
              Read more about Rebecca J. Cole
                <a href="https://www.smithsonianmag.com/science-nature/woman-challenged-idea-black-communities-destined-disease-180969218/" target="_blank" >here</a>.
            </ArticleText>


        {/snippet}
    </Scroller>
    </div>
</div>

<style>
    #picture {
        padding: 0px;
        width: 550px;
        overflow: auto;
        align-items: right;
    }
     .box {
        vertical-align: top;
        text-align: right;
    }
     .scrolling{
       height: 7500px;
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
        height: 0px;
        vertical-align: bottom;
        font-size: large;
    }
    h1{
        vertical-align: bottom;
        margin-top: 20%;
        font-size: 50px;
    }
</style>

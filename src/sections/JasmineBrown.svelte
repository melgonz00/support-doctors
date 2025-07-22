<script>
import Scroller from "../lib/Scroller.svelte";
import ArticleText from "../lib/ArticleText.svelte";
</script>
<div id="title">
    <h1>
        Jasmine Brown
    </h1>
</div>
<div>
    <div class="scrolling">
    <Scroller layout="right">
        {#snippet sticky()}
            <div class="box">
                <img id="picture" src="jasminebrown.png" alt="brown">
            </div>
            <p>Image Source: <a href="https://www.jasminebrownauthor.com/" target="_blank">Jasmine Brown</a></p>
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                In 2023, Jasmine Brown was a third-year medical student at the University of Pennysvania when 
                she released her book “Twice as Hard,” motivated by her own difficult experiences in being a Black student. 
            </ArticleText>

            <ArticleText>
               In an interview with Word In Black, she mentions that within her AP and colleges classes, 
               she was the only Black student and faced discrimincation from her peers.<sup>12</sup>
            </ArticleText>

            <ArticleText>
                Brown’s book highlights the stories of different female Black physicians throughout history, including Rebecca Lee Crumpler.

            </ArticleText>

            <ArticleText>
                Brown hopes that the stories in her book will inspire more Black girls to become physicians 
                and influence readers to address the issues that continue to face Black doctors.<sup>12</sup>
            </ArticleText>

            <ArticleText>
              Read more about Jasmine Brown
                <a href="https://wordinblack.com/2023/02/twice-as-hard-why-entering-medicine-has-never-been-easy-for-black-women/" target="_blank" >here</a>.
            </ArticleText>


        {/snippet}
    </Scroller>
    </div>
</div>

<style>
    #picture {
        padding: 0px;
        width: 600px;
        overflow: auto;
        align-items: left;
    }
     .box {
        vertical-align: top;
        text-align: left;
    }
     .scrolling{
       height: 5300px;
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
        padding: 2%;
        height: 0px;
        vertical-align: right;
        font-size: large;
    }
    p{
        color: white;
    }
    h1{
        text-align: right;
        vertical-align: bottom;
        margin-top: 20%;
        font-size: 50px;
    }
</style>

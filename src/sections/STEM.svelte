<script>
    import * as Highcharts from "highcharts";
    import "highcharts/modules/exporting";
    import { Chart } from "@highcharts/svelte";
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";

    let chart;

    let options = {
    chart: {
        type: 'column',
            borderColor: "#9798af",
            borderWidth: 5,
            borderRadius: 20,
    },
    title: {
        text: 'STEM Employment Rates Among 25-34 Year Olds with a STEM Degree as of 2021'
    },
    subtitle: {
        text:
            'Source: <a target="_blank" ' +
            'href="https://blackwealthdata.org/explore/education">Black Wealth Data Center</a>'
    },
    xAxis: {
        categories: ['Asian', 'Black', 'Hispanic', 'White'],
        crosshair: true,
        accessibility: {
            description: 'Race/Ethnicity'
        }
    },
    yAxis: {
        min: 0,
        max: 100,
        title: {
            text: 'Percent Working in STEM (%)'
        }
    },
    plotOptions: {
        column: {
            pointPadding: 0.2,
            borderWidth: 0
        }
    },
    series: [
        {
            name: "Female",
            data: [48.2,20.7,26.4,28.8
            ],
            color: "#dbd5d9",
        },
        {
            name: "Male",
            data: [62.8,41.5,26.4,51.2
            ],
            color: "#545454",
        },
    ]
}

</script>

<div>
    <div class="scrolling">  
    <Scroller layout="left">
        {#snippet sticky()}
            <div class="chart">
                <Chart bind:chart {options} highcharts={Highcharts} />
            </div>
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                We still struggle to support Black students, especially Black women in STEM.
            </ArticleText>
            <ArticleText> 
             Only 20.7% of Black women with a STEM degree are working in a STEM-related field.
            </ArticleText>
            <ArticleText> 
            We have to do better.
            </ArticleText>

           

        {/snippet}
    </Scroller>
    </div>
</div>

<style>
    .chart {
        width: 90%;
        margin: 0px auto;
    }
     .scrolling{
       height: 3800px;
       background-color: black;
    }
</style>

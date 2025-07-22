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
        text: 'Number of Active MD Residents as of 2024'
    },
    subtitle: {
        text:
            'Source: <a target="_blank" ' +
            'href="https://blackwealthdata.org/explore/employment">Black Wealth Data Center</a>'
    },
    xAxis: {
        categories: ['Total', 'Asian', 'Black', 'Hispanic', 'White'],
        crosshair: true,
        accessibility: {
            description: 'Race/Ethnicity'
        }
    },
    yAxis: {
        min: 0,
        title: {
            text: 'Count of Active MD Residents'
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
            name: "Total",
            data: [260610
            ],
            color: "black",
        },
        {
            name: "Asian",
            data: [60730
            ],
            color: "#545454",
        },
        {
            name: "Black",
            data: [
                17964
            ],
            color: "#867e7e",
        },
        {
            name: "Hispanic",
            data: [
                23080
            ],
            color: "#dbd5d9",
        },
        {
            name: "White",
            data: [
                123036
            ],
            color: "#bdb1bb",
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
                However, according to the Black Wealth Data Center, 
                <br> only <strong>6.9%</strong> of active MD residents are Black. 
            </ArticleText>
            <ArticleText> 
             Meanwhile, in 2023, an estimated 48.3 million people self-identified as Black, 
            making up 14.4% of the country’s population.<sup>4</sup>
            </ArticleText>
            <ArticleText> 
            The ratio of Black physicians to Black Americans is disproportionate.
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

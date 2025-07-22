<script>
    import * as Highcharts from "highcharts";
    import "highcharts/modules/exporting";
    import { Chart } from "@highcharts/svelte";
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";

    let options = {
        chart: {
            type: "pie",
            borderColor: "#9798af",
            borderWidth: 5,
            borderRadius: 20,
        },
        title: {
            text: "Distribution of Specialties with Black Residents",
        },
        plotOptions: {
            pie: {
                allowPointSelect: true,
                dataLabels: [
                    {
                        enabled: true,
                        distance: 20,
                    },
                    {
                        enabled: true,
                        distance: -40,
                        format: "{point.percentage:.1f}%",
                        style: {
                            fontSize: "1.2em",
                            textOutline: "none",
                            fontFamily: "Georgia"
                        },
                        filter: {
                            operator: ">",
                            property: "percentage",
                            value: 10,
                        },
                    },
                ],
            },
        },
        series: [
            {
                name: "Count of Black Residents (2024)",
                data: [
                    {
                        name: "Specialties with 0 Black Residents",
                        color: "#545454",
                        y: 35,
                    },
                    {
                        name: "Specialties with 10 or Less Black Residents*",
                        color: "#867e7e",
                        y: 84,
                    },
                    {
                        name: "Specialties with more than 10 Black Residents",
                        color: "#dbd5d9",
                        y: 59,
                    },
                ],
            },
        ],
    };
</script>
<div>
    <div class="scrolling"> 
    <Scroller layout="right">
        {#snippet sticky()}
            <div class="chart">
                <Chart {options} highcharts={Highcharts} />
            </div>
            <p>
                *Excludes specialties with 0 Black Residents.
            </p>
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                Additionally, <strong>more than half</strong> of medical <br> specialties/sub-specialties 
                have 10 or less active Black residents.
            </ArticleText>

            <ArticleText>
                Almost 20% of medical specialties/sub-specialties have 
                <strong>no active Black residents working in them</strong>.
            </ArticleText>

            <ArticleText>
                Although some specialites are very niche, such as Aerospace Medicine, it is important to have diverse representation in <strong>all</strong> fields of medicine.
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
    p{
        color: white;
    }
    .scrolling{
       height: 3800px;
       background-color: black;
    }
</style>
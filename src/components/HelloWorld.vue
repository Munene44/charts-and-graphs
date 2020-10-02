
Skip to content
Pull requests
Issues
Marketplace
Explore
@Munene44
Learn Git and GitHub without any code!

Using the Hello World guide, you’ll start a branch, write comments, and open a pull request.
ratracegrad /
vue-eCharts-demo

1
11

    5

Code
Issues
Pull requests
Actions
Projects
Wiki
Security

    Insights

vue-eCharts-demo/src/components/HelloWorld.vue
@ratracegrad
ratracegrad first commit
Latest commit 93117cf on Apr 7, 2019
History
1 contributor
87 lines (85 sloc) 1.44 KB
<template>
  <div>
    <div class="chart-wrapper">
      <chart :options="chartOptionsBar"></chart>
    </div>
    <hr />
    <div class="chart-wrapper">
      <chart :options="chartOptionsLine"></chart>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data: () => ({
    chartOptionsBar: {
      xAxis: {
        data: ["Q1", "Q2", "Q3", "Q4"]
      },
      yAxis: {
        type: "value"
      },
      series: [
        {
          type: "bar",
          data: [63, 75, 24, 92]
        }
      ],
      title: {
        text: "Quarterly Sales Results",
        x: "center",
        textStyle: {
          fontSize: 24
        }
      },
      color: ["#127ac2"]
    },
    chartOptionsLine: {
      xAxis: {
        data: [
          "Jan",
          "Feb",
          "Mar",
          "Apr",
          "May",
          "Jun",
          "Jul",
          "Aug",
          "Sep",
          "Oct",
          "Nov",
          "Dec"
        ]
      },
      yAxis: {
        type: "value"
      },
      series: [
        {
          type: "line",
          data: [55, 72, 84, 48, 59, 62, 87, 75, 94, 101, 127, 118]
        }
      ],
      title: {
        text: "Monthly Stock Prices",
        x: "center",
        textStyle: {
          fontSize: 24
        }
      },
      color: ["#127ac2"]
    }
  })
};
</script>

<style scoped>
.chart-wrapper {
  width: 100%;
  height: 700px;
}
.echarts {
  width: 100%;
  height: 100%;
}
</style>

    © 2020 GitHub, Inc.
    Terms
    Privacy
    Security
    Status
    Help

    Contact GitHub
    Pricing
    API
    Training
    Blog
    About


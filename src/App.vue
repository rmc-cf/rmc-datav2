<template>
  <dv-full-screen-container>
    <RmcDvChart :option="option1" />
    <RmcRingChart :config="config1" />
    <RmcCapsuleChart :config="config1" />
    <RmcWaterLevel :config="config2" />
    <RmcWaterLevel :config="config3" />
    <RmcWaterLevel :config="config4" />
    <RmcPercentPond/>
    <RmcFlylineChart/>
    <RmcConicalColumn/>
  </dv-full-screen-container>
</template>

<script>
import RmcDvChart from './components/RmcDvChart.vue'
import RmcRingChart from './components/RmcRingChart.vue'
import RmcCapsuleChart from './components/RmcCapsuleChart.vue'
import RmcWaterLevel from './components/RmcWaterLevel.vue'
import RmcPercentPond from './components/RmcPercentPond.vue'
import RmcFlylineChart from './components/RmcFlylineChart.vue'
import RmcConicalColumn from './components/RmcConicalColumn.vue'

const option1 = {
  title: {
    text: '剩余油量表',
    style: {
      fill: '#fff'
    }
  },
  series: [
    {
      type: 'gauge',
      data: [{ name: 'itemA', value: 55 }],
      center: ['50%', '55%'],
      axisLabel: {
        formatter: '{value}%',
        style: {
          fill: '#fff'
        }
      },
      axisTick: {
        style: {
          stroke: '#fff'
        }
      },
      animationCurve: 'easeInOutBack'
    }
  ]
}
const config1 = {
  data:[
    {
      name: '周口',
      value: 55
    },
    {
      name: '南阳',
      value: 120
    },
    {
      name: '西峡',
      value: 78
    },
    {
      name: '驻马店',
      value: 66
    },
    {
      name: '新乡',
      value: 80
    }
  ],
  colors: ['#e062ae', '#fb7293', '#e690d1', '#32c5e9', '#96bfff'],
  unit: '单位',
  showValue: true
}
const config2 = {
  data:[52,24],
}
const config3 = {
  data:[52,24],
  shape:'roundRect'
}
const config4 = {
  data:[52,24],
  shape:'round'
}

export default {
  name: 'App',
  components: {
    RmcDvChart,
    RmcRingChart,
    RmcCapsuleChart,
    RmcWaterLevel,
    RmcPercentPond,
    RmcFlylineChart,
    RmcConicalColumn

  },
  data() {
    return {
      option1,
      config1,
      config2,
      config3,
      config4,
    }
  },
}
</script>

<style>
#dv-full-screen-container{
  background-color: #000;
  display: flex;
  padding: 20px 10px;
  gap: 20px;
  justify-content: space-between;
  flex-wrap: wrap;
}
</style>

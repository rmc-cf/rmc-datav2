<template>
  <dv-full-screen-container>
    <RmcDvChart :option="option1" />
    <RmcRingChart :config="config1" />
    <RmcCapsuleChart :config="config1" />
  </dv-full-screen-container>
</template>

<script>
import RmcDvChart from './components/RmcDvChart.vue'
import RmcRingChart from './components/RmcRingChart.vue'
import RmcCapsuleChart from './components/RmcCapsuleChart.vue'
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

export default {
  name: 'App',
  components: {
    RmcDvChart,
    RmcRingChart,
    RmcCapsuleChart
  },
  data() {
    return {
      option1,
      config1,
    }
  },
}
</script>

<style>
#dv-full-screen-container{
  background-color: #000;
  display: flex;
  padding: 10px;
}
</style>

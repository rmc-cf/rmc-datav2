<template>
       <dv-conical-column-chart :config="config" style="width:400px;height:200px;" />
</template>
<script>
export default {
       props: {
              config: {
                     type: Object,
                     default: () => ({
                            data: [{
                                   name: '周口',
                                   value: 55
                            },
                            {
                                   name: '南阳',
                                   value: 120
                            }],
                            img: ['/favicon.ico'],//
                            showValue: true
                     })
              }
       },
       components: {
       },

}
</script>
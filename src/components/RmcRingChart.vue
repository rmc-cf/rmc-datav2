<template>
       <dv-active-ring-chart :config="config" style="width:300px;height:300px" />
</template>
<script>
export default {
       props: {
              config: {
                     type: Object,
                     default: () => ({})
              }
       },
       components: {
       },
    
}
</script>
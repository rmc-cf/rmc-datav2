<template>
    <dv-percent-pond :config="config" style="width:200px;height:100px;" />
</template>
<script>
export default {
       props: {
              config: {
                     type: Object,
                     default: () => ({
                            value:66
                     })
              }
       },
       components: {
       },
    
}
</script>
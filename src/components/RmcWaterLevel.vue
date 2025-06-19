<template>
       <dv-water-level-pond :config="config" style="width:150px;height:200px" />
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
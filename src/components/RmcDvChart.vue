<template>
       <dv-charts :option="option"  style="width:300px;height:300px"/>

</template>

<script>
export default {
       props: {
              option: {
                     type: Object,
                     default: () => ({})
              }
       },
       components: {
       },
    
}
</script>
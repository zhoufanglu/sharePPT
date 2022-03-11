<div id="left">

### ✰ VUE2
```javascript
export default {
  beforeCreate() {},
  
  created() {},
  
  beforeMount() {},
  
  mounted() {},
  
  beforeUpdate() {},
  
  updated() {},
  
  beforeDestroy() {},
  
  destroyed() {},
}
```

</div>

<div id="right">

### ✧ VUE3
``` javascript
export default {
  setup() {
 
    onBeforeMount(_=>{})
    
    onMounted(_=>{})
    
    onBeforeUpdate(_=>{})
    
    onUpdated(_=>{})
    
    onBeforeUnmount(_=>{})
    
    onUnmounted(_=>{})
  }
}
```

</div>

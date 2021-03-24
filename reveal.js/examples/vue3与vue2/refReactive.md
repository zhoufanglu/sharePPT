<div id="left">

### ✰ ref
```javascript
export default {
  setUp() {
    /**********************ref***********************/
    let num = ref<number>(1)
    console.log(19, num) //变成这种Proxy({num: 1})形式
    
    setTimeout(_=>{
      num.value = 0
    },1000)

    return {
      num,
    }
  }
  
}
```

</div>

<div id="right">

### ✧ reactive， toRefs
```javascript
function reactive<T extends object>(target: T): UnwrapNestedRefs<T>
```
``` javascript
export default {
/**********************reactive***********************/
    interface Person {
      name: string,
      gender: string
    }

    let person = reactive<Person>({
      name: 'aaa',
      gender: 'male' 
    })
    console.log(33, person) //Proxy{name: 'lufangzhou', gender:'male'}
    //person.name = 'bbb'
    setTimeout(_=>{
      person.name = 'bbb'
    })
    //解构
    //toRefs , 原本是proxy({name: 'lufangzhou', gender:'male'})
    //可以用来为源响应式对象上的 property 性创建一个 ref。然后可以将 ref 传递出去，从而保持对其源 property 的响应式连接。
    const {name, gender} = toRefs(person)
    return {
      name,
      gender
    }
}
```

</div>

<div id="left"> 

#### 代码 
```javascript
Mock.mock('/store/test',{
  
    title: Random.ctitle(),
  
    date: Random.date('yyyy-MM-dd'),
  
    "id|+1": 1,
  
    img: Random.image(Random.size, '#02adea', 'Hello')
  
})
```
</div>

<div id="right">

#### 输出 
```javascript
{
  
  title: "准学阶有"
  
  date: "1998-10-21"
  
  id: 1
  
  img: "http://dummyimage.com/240x400/02adea&text=Hello"
  
}
```

</div>

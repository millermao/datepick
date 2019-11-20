# calendar vue日期选择组件

## 介绍

>一个选择日期的vue组件

## 组件使用

>安装

```bash
npm i datepick-haiyin --save
```

>初始化

```js
import Calendar from 'datepick-haiyin';
Vue.use(Calendar);
```

>使用

```js
 <script>

 export default {
   name: 'App',
   data(){
       return{
           date:'',
           date2:'2010-3-2'
         }
   },
   methods:{
     setDate(){

       this.$picker.show({
         type:'datePicker',
         onOk: (date) =>{
           this.date = date
         }
       });

     },
     setDate2(){

       this.$picker.show({
         type:'datePicker',
         date:this.date2,  //初始化时间
         endTime:'2020-02-11',  //截至时间
         startTime:'2010-02-11',  //开始时间
         onOk:(e)=>{
           this.date2 = e;
         },

       })

     },

   },

 }
 </script>




``` 

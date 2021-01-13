# Mixin

我们在日常开发中经常遇到多个页面或者功能模块有相同代码逻辑的情况，同学们在遇到此类情况的时候肯定会想：如果这段代码能够复用就好了！。那什么方法可以帮助我们实现复用呢？答案就是：Mixin！ Mixin 帮助我们抽离公共代码逻辑。一个混入对象可以包含任意组件选项。当组件使用混入对象时，所有混入对象的选项将被 “混合” 进入该组件本身的选项。

## 定义一个Mixin

mixin 本质上就是一个 Object 对象，它和 vue 实例上的属性一致，包含 data、methods、computed、watch、生命周期函数等等：

```js
var myMixin = {
    data(){
        return{

        }
    },
    created(){

    },
    methods:{

    },
    computed(){

    }
}
```

## 混入Mixin

想要混入定义好的 mixin，只需要通过组件的 mixins 属性传入想要混入的 mixin 数组即可：

```js
var vm = new Vue({
    el: '#app',
    mixins:[myMixin]
})
```

### 全局混入

```js
Vue.mixin({
  data: {
    name: "Imooc"
  }
})
```

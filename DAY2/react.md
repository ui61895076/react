###REACT 组件
不管是vue还是react框架，设计之初都是期望我们按照“组件、模块管理 的”方式来构建程序的，也就是把一个程序划分为一个个的组件来单独处理
【优势】
 1，有助于多人协助开发；
 2，开发的组件可以复用

REACT中创建组件有两种方式：
1，函数声明组件 this指向的是undefined
2，基于继承COMPONENT类来创建组件 this指向的是类的实例，也就这个自定义的组件

SRC ->COMPONENT :这个文件夹中存放的就是开发组件

知识点：React.createElemtent 在处理 的时候遇到一个组件，返回的对象中type 不是字符串标签名了，而是以个函数（类）
但是 属性还是存在 props中


注意地方：1，写样式在外面的时候 比如 let sstyle={width:"12px"}值需要加引号
          2，在组件定义 属性的时候 例如 <Dialog type={2}/> 如果是数字类型  必须要用{}


 2,基于继承component类来创建组件

总结：创建组件有两种方式“函数式”，“创建类式”
【函数式】
1，简单
2，能实现的功能也简单，只是简单的调取和返回jsx而已

【类式】
1，操作相对复杂，但是也可以实现更为复杂的业务功能
2，能够使用生命周期函数操作业务
3，函数式可以理解为静态组件（组件中的内容调取的时候就已经固定了，很难再修改），而类这种方式，可以基于组件内部的状态来更新渲染的内容；

类创建组件的是时候，传递进来的props属性只能读不能修改，但是我们可以通过
static defaultProps{}创建出一个默认值 当this.props中有属性 没有定义的 可以通过默认值去设置


在组件数据props 中除了自定义 的数据外，还有一个属性是children 他的值是在自定义组件标签中写的东西例如 <child>我是children属性的值</child>
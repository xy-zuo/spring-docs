## 1. IOC容器

本章涵盖了Spring的控制反转(IoC)容器

### 1.1 Spring IOC容器和beans说明

这一章涵盖了Spring框架对于控制翻转(IoC)原则的实现。Ioc也被称为依赖注入(DI)。它是一个过程：对象定义它们的依赖（它们使用的其他对象）仅仅通过构造器参数、或者在工厂方法里的参数或者是在创造出对象实例（通过构造方法或者工厂方法）后进行设置属性，然后容器在创建bean时注入那些依赖。这个过程从根本上翻转了普通的创建对象的过程（通过直接构造类或Service Locator的模式来控制依赖关系的实例化或位置）。



`org.springframework.beans`和`org.springframwork.context`是Spring 框架中IoC容器的基础。[`BeanFactory`](url::BeanFactory)接口提供了一种能够管理任何类型的对象的、更加先进的配置机制。

[`ApplicationContext`](url::ApplicationContext) 是`BeanFactory`的子接口。它添加了：

- 更容易与Spring的AOP特性集成
- 消息资源处理（用于国际化）
- 事件发布
- 应用层特定的上下文，如用于web应用的`WebApplicationContext`

总之，`BeanFactory`提供了配置框架和基础功能，`ApplicationContext`添加了更多特定于企业的功能。`ApplicationContext`完全扩展了`BeanFactory`的功能，并且仅在本章中用于描述Spring IoC容器。关于使用`BeanFactory`而非`ApplicationContext`的更多信息，请参考 [`The BeanFactory`]()一栏。



### 1.16 BeanFactory


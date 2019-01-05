# 工厂模式
工厂模式专门负责将大量有共同接口的类实例化，这里的共同接口也可以理解为所做的事情都类似（比如数据库操作的dao接口可以理解为共同接口）；  
一般而言，一个系统总是可以抽象成产品的消费者角色、产品的工厂角色、产品角色三个子系统；在spring框架里，产品的工厂角色就是spring容器本身，产品角色与产品的消费者角色已经你中有我，我中有你了；
## 简单工厂模式
静态工厂方法模式  
个人觉得spring的BeanFactory就是简单工厂模式的一个实现
## 工厂方法模式
个人觉得spring的FactoryBean就是工厂方法模式的一个实现
## 抽象工厂模式
考虑如下场景：抽象出第三方接口提供者的BeanFactory（理解父子BeanFactory的概念），系统里有BeanFactory-salA、BeanFactory-salB....，然后根据配置文件决定是使用BeanFactory-salA还是BeanFactory-salB，这个时候使用的就是抽象工厂模式
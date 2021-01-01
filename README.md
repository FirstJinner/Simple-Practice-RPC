# Simple-Practice-RPC
+ 概述：
以注解驱动的形式，客户端实现服务远程调用，服务端发布服务
+ 客户端：
1. 客户端实现@Reference注解，通过实现BeanPostProcessor接口，在spring启动时，为服务实例创建代理对象
2. 代理对象通过TCP连接向服务器获取服务结果
+ 服务端：
1. @RemoteService发布服务，通过实现BeanPostProcessor接口，在spring启动时，把实例对象注入map容易作为路由
+ 协议

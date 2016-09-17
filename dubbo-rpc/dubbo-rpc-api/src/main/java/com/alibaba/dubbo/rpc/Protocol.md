Protocol代表协议，用于RPC的协议抽象。必须是ThreadSafe的。协议需要完成Invoker的封装工作。
*****
- export(Invoker invoker)
  - 用于暴露对外提供的服务；此方法的实现必须是幂等的，即多次调用方法暴露服务与一次暴露服务是一样的。
- refer(Class<T> type, URL url)
  - 用于引用远程服务的；调用方法会返回由协议封装的Invoker方法，后用户调用Invoker的invoke实现远程方法的调用。Invoker封装了远程调用的细节。


  APPACH  COMMON IBATIS MYBATIS SPRING WEBX

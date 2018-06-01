# Java异常处理

## Java异常处理规范
### 原则：

#### 1. 不要直接catch Exception这样的通用异常,捕获指定的特定异常
捕获所有异常一般是不负责任的表现

#### 2. 不要生吞(swallow)异常

#### 3. 使用自定义异常替代返回值枚举
因为返回值的枚举会造成依赖磁铁,违反开闭原则,所有类都必须要依赖这个枚举,改变这个枚举必须编部署所有类。使用自定义异常,使用继承体系会打破这种依赖。

#### 4. 不要使用checkedException
除非你有非常合适的理由,否则不要使用checkedException
* 因为很多时候并不能恢复现场
* 打破了方法和类的封装性。

#### 5.错误处理不要使用printStack记录

### 建议：
> throw early, catch later

尽早的检查抛出异常,在最后统一的处理异常。


## SpringMvc中处理异常规范

### 原则

1. 对于自定义的异常,使用 **@ResponseStatus** 
2. 如果是通用的异常,比如没有权限访问,参数不正确等,使用 **@ControllerAdvice**中 **@ExceptionHandler**统一处理。
3. 如果是某个controller中才有的异常,比如某个需要的文件不存在,在controller中定义 **@ExceptionHandler**。

注意：
>对于处理相同的异常,在controller中定义的@ExceptionHandler会比@ControllerAdvice中的优先级高。

>https://spring.io/blog/2013/11/01/exception-handling-in-spring-mvc
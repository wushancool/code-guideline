# Java�쳣����

## Java�쳣����淶
### ԭ��

#### 1. ��Ҫֱ��catch Exception������ͨ���쳣,����ָ�����ض��쳣
���������쳣һ���ǲ������εı���

#### 2. ��Ҫ����(swallow)�쳣

#### 3. ʹ���Զ����쳣�������ֵö��
��Ϊ����ֵ��ö�ٻ������������,Υ������ԭ��,�����඼����Ҫ�������ö��,�ı����ö�ٱ���ಿ�������ࡣʹ���Զ����쳣,ʹ�ü̳���ϵ���������������

#### 4. ��Ҫʹ��checkedException
�������зǳ����ʵ�����,����Ҫʹ��checkedException
* ��Ϊ�ܶ�ʱ�򲢲��ָܻ��ֳ�
* �����˷�������ķ�װ�ԡ�

#### 5.������Ҫʹ��printStack��¼

### ���飺
> throw early, catch later

����ļ���׳��쳣,�����ͳһ�Ĵ����쳣��


## SpringMvc�д����쳣�淶

### ԭ��

1. �����Զ�����쳣,ʹ�� **@ResponseStatus** 
2. �����ͨ�õ��쳣,����û��Ȩ�޷���,��������ȷ��,ʹ�� **@ControllerAdvice**�� **@ExceptionHandler**ͳһ����
3. �����ĳ��controller�в��е��쳣,����ĳ����Ҫ���ļ�������,��controller�ж��� **@ExceptionHandler**��

ע�⣺
>���ڴ�����ͬ���쳣,��controller�ж����@ExceptionHandler���@ControllerAdvice�е����ȼ��ߡ�

>https://spring.io/blog/2013/11/01/exception-handling-in-spring-mvc
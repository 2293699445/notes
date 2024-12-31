# javaweb

### 1、深度剖析转发和重定向的区别 

* 代码上

  * 转发

    ``````java
    //获取转发器对象
    RequestDispatcher dispatcher = request.getRequestsDispatcher();
    //调用转发器对象的forward方法实现转发
    dispatcher.forward(request,response);
    //不管转发多少次，都是同一次请求，使用的都是同一个request和response对象，在tomcat内部转发
    ``````

  * 重定向

    ``````java
    //路径上要加项目名，相当于浏览器前端发请求给服务器（前端往后端发请求都是带项目名）
    //相当于把这个路径返回给浏览器，浏览器拿到这个路径再去请求
    response.sendRedirect("/oa/dept/list");
    ``````



* 形式上 	
  * 转发：一次请求，浏览器请求路径http://localhost:8080/oa/dept/a，转发结束后路径不变，刷新网页会请求多次，造成重复操作。
  * 重定向：两次请求，浏览器请求路径http://localhost:8080/oa/dept/a，重定向后路径会变，http://localhost:8080/oa/dept/b
* 本质上
  * 转发：WEB服务器控制转发，A资源跳转B资源，跳转动作是在服务器内部完成的。两个资源共享同一个request和response对象
  * 重定向：浏览器完成重定向操作，具体跳转到哪个资源，由浏览器说了算。两个资源享用的request和response对象不是同一个
* 使用上
  * 转发：两资源要使用同一个域中的数据，就用转发机制。其他都用重定向。
  * 重定向：可以解决405报错问题。请求是post方法，转发到另外一个资源还是用的post方法，如果这个资源里只写了doGet方法，就会报405错误。使用重定向可以解决这个问题，因为浏览器发的是get方法。

### 2、request和response中的常用方法有哪些？

3、详细说明请求域和应用域是什么？

4、webServlet注解释开发 跟web.xml的区别？

5、模板方法是如何解决类爆炸问题的？

6、JSP是啥，JSP的原理？ 



### context:component-scan标签
在xml文件配置了<context:component-scan>标签后，spring容器可以自动去扫描base-pack所指定的包或其子包下面的java类文件，如果扫描到有@Component、@Controller、@Service 、@Repository等注解修饰的Java类，则将这些类注册为spring容器中的bean。

如果手动在xml文件中注入了某个目录下的所有bean，那么就不需要该标签了。
## spring
spring的核心配置文件是applicationContext.xml，spring-dao.xml,spring-mvc.xml,spring-service.xml这些配置文件最后都需要import到这里。之所以分成这么多配置文件不直接在applicationContext.xml里写是为了方便。
### spring-service.xml
service层涉及到的业务代码可能比较复杂，需要配置一些事务相关的信息。
## springmvc
### spring-mvc.xml
为了将springmvc整合到spring中，需要在spring配置文件中配置一些信息，这些配置信息单独写在spring-mvc.xml中。
### web.xml
web.xml中可定义DispatcherServlet，filter等组件。
总配置文件applicationContext.xml需要引入到web.xml初始化xmlDispatcherServlet。
## mybatis
### mybatis-config.xml
mybatis的核心配置文件是mybatis-config.xml，通常作用是注册众多mapper文件。
mybatis-config.xml文件名可以改成别的。resources目录下的所有配置文件都是会自动加载的，通过文件头内容可以识别出这是mybatis的核心配置文件。
### spring-dao.xml
为了将mybatis整合到spring中，需要将一些配置信息写在spring-dao.xml中。
### database.properties
为了方便，数据库的配置信息可以单独放在一个文件，最后将该文件引入到spring-dao.xml中。
## 注解

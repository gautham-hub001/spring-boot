# spring-boot

continuation

For working with .jsp files, you need to add a dependency: tomcat jasper(JSP Parser).
Goto mvnrepository.com and search for jasper and check the version of the embedded tomcat in your project and click on the same versdion of jasper from here and copy the dependency code for maven and paste it in your pom.xml file.

Now, spring boot can cnvert the jsp into servlet.


The webapp folder we're using is public.
To make it private:
1. Create a sub folder inside webapp called as pages and move home.jsp to pages
2. change return "home.jsp" to "home"
3. Open applicaiton.properties file and here we'll mention prefix and suffix:
  spring.mvc.view.prefix=/pages/
  spring.mvc.view.suffix=.jsp
  
We can also use .yaml file instead of application.properties but only in application.preoperties we can mention all the properties


**Getting data from user (Dynamic page):**
You want to create a dynamic page which takes user name and displays it on the page.
eg: localhst:8080/home?name=gautham

In your HomeController:
public String home(HttpServletRequest req){
  String name = req.getParameter("name");
}

Watch Servlet videos: requestDispatcher

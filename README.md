# Java Servlet & Jsp
Learning notes about Java Servlet and JSP

## Dynamic Web Project
* Java Resources: place Servlets
* WebContent: place JSP, HTML

# Servlet
## Methods
### doGet
```
protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException e {
    PrintWriter print = response.getWriter();
    print.println("<h1>Hello World</h1>");
}
```
## Life Cycle


# JSP
Implicitly converted into Servlet

## JSP Scripting Element
### Expression
only one single statement  
`<%= out.println("Hello World") %>`  
`<%= new String("Jian") %>` or `<%= "Jian" %>`  
`<%= new java.util.Date() %>`  
`<%= 25 * 10 %>`  
`<%= 25 > 50 %>`  

### Scriptlet
`<% out.println("Hello World"); %>`  
`<% if(25>50) { out.println("True"); } else { out.println("False"); } %>`  
```
<%
int age = 12;
out.println("My age is: " + age);
%>
```

### Declaration
```
<%! public int x=5; %>
<%= x %>
```
```
<%! 
String message() {
    return "Hello World";
}
%>
<%= message() %>
```
### Directive
A JSP directive privides additional information about the page to JSP Engine at page traslation time. This addtional information is used by JSP container and it controls the processing of the entire page accordingly. 

#### Page Directive
#### Taglib Directive
#### include Directive

### Comment

# Citation
JSP and servlet basics, Udemy, https://www.udemy.com/jsp-servlet-free-course/learn/v4/overview

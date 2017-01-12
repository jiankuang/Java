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
### Comment


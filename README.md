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
`<%= out.println("Hello World") %>`  
`<%= new String("Jian") %>` or `<%= "Jian" %>`  
`<%= new java.util.Date() %>`  
`<%= 25 * 10 %>`  
`<%= 25 > 50 %>`  

### Scriptlet
`<% if(25>50) { out.println("True"); } else { out.println("False"); } %>`

### Declaration
```
<%! public int x=5; %>
<%= x %>
```
### Directive
### Comment


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

# JSP

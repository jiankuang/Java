# Java Web
## JSP
### JSP Implicit Objects
request : `request.getParameter("myparameter")`  
session : `session.getCreationTime()`  
application : `application.getAttribute("ApplicationWideAttribute")`  
out : PrintWriter object used to send output to the client  
config : ServletConfig object `config.getServletName()`  
pageContext : `pageContext.getServletContext()`  
response : `response.setHeader("Pragma", "no-cache")`  
page : `page.getClass()`  
### getParameter('parameter') vs getAttribute('attribute')
`getParameter` is used to get value from Form elements, return `String`  
`getAttribute` return `Object`

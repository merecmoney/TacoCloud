# Notes

## Dependency Injection

Dependency injection is a technique in which an object receives other
objects that it depends on. These other objects are called dependencies.

The "injection" refers to the passing of a dependency (a service) into
the object (a client) that would use it.

## Spring MVC

### Controller

A class that handles requests and responds with information of some sort.

In the case of a web application, a controller responds by optionally
populating model data and passing request on to a view to
produce HTML that's returned to the browser.

Handle HTTP request and either hand the request off to a view to render HTML
(browser-displayed) or write data directly to the body of a response(RESTful).

### @WebMvcTest

This  is a special test annotation provided by Spring Boot
that arranges for the test to run in
the context of a Spring MVC application

@WebMvcTest also sets up Spring support for testing Spring MVC.

Spring automatically:

- Configures the beans in the Spring application context to enable Spring MVC
- Configures the embedded Tomcat server in the Spring application context
- Configures a Thymeleaf view resolver for rendering Spring MVC views with
Thymeleaf templates

## Spring Boot

Offers started dependencies and autoconfiguration.


The @Request-
Mapping annotation, when applied at the class level,
specifies the kind of requests that
this controller handles. In this case,
it specifies that DesignTacoController will handle
requests whose path begins with /design.

The class-level @RequestMapping specification is refined with the @GetMapping annota-
tion that adorns the showDesignForm() method. @GetMapping , paired with the class-
level @RequestMapping , specifies that when an HTTP GET request is received for
/design, showDesignForm() will be called to handle the request.

Model is an object that ferries data
between a controller and whatever view is charged with rendering that data.

Ulti-
mately, data that’s placed in Model attributes is copied into the servlet response attri-
butes, where the view can find them.


View libraries such as Thymeleaf are designed to be decoupled from any particular
web framework. As such, they’re unaware of Spring’s model abstraction and are
unable to work with the data that the controller places in Model . But they can work
with servlet request attributes. Therefore, before Spring hands the request over to a
view, it copies the model data into request attributes that Thymeleaf and other view-
templating options have ready access

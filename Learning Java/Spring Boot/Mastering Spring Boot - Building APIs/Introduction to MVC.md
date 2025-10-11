
In this section I explored Spring MVC, the web framework built into Spring Boot that allows us to build both traditional web applications and modern REST APIs.
I learned about web key concepts, the MVC design pattern, and how Spring Boot handles HTTP requests.

## How the Web Works

When we browse a website, our browser (the client) sends a request to a server. The server processes the request and returns a response.

This communication happens using HTTP (Hyper-Text Transfer Protocol), which defines how data  is exchanged over the web.

## Key Parts of an HTTP Request

- **Method** - Specifies what action we want to perform (GET, POST, PUT, PATCH, DELETE)
- **URL** - The address of the resource being requested
- **Headers** - Extra information (e.g. content type, authentication tokens)
- **Body** - Contains data for the server (e.g. form submissions)

## Key Parts of an HTTP Response

- **Status Code** - Indicates if the request was successful (200 OK, 404 Not Found)
- **Headers** - Metadata about the response
- **Body** - The actual content returned by the server, it can contain
	- **HTML Markup** used in traditional web applications
	- **Data in JSON Format** used in APIs

## How Web Pages are Generated

Web pages are built using HTML (Hyper-Text Markup Language). In web applications HTML can be generated in two ways.
- **On the Server** - The server generates the full HTML page and sends it to the client. This technique is referred to as **Server-Side Rendering (SSR)**
- **On the Client** - The server send only raw data (JSON), and the client dynamically generates the web page using JavaScript. This technique is referred to as **Client-Side Rendering (CSR)**

## What is JSON?

**JSON (JavaScript Object Notation)** is a lightweight format used to structure data. It is commonly used in APIs because it is easy to read and process for both humans and computers.

## What is an API?

**API (Application Programming Interface)** is a way for applications to communicate with each other.
In web development, an API allows a client (browser, mobile app, or another system...) to send/request data to/from a server.

## Spring MVC

Spring MVC follows the Model-View-Controller (MVC) pattern, which organizes web applications into three parts
- **Model** - Represents data and business logic. Typically, these are Java objects mapped to database entities (below is an example of a User Model)
	```java
	@Builder  
	@AllArgsConstructor  
	@NoArgsConstructor  
	@Getter  
	@Setter  
	@Entity  
	@Table(name = "users")  
	public class User {  
	  @Id  
	  @GeneratedValue(strategy = GenerationType.IDENTITY)  
	  @Column(name = "id")  
	  private Long id;  
	  
	  @Column(name = "name")  
	  private String name;  
	  
	  @Column(name = "email")  
	  private String email;  
	  
	  @Column(name = "password")  
	  private String password;  
	  
	  @OneToMany(mappedBy = "user")  
	  @Builder.Default  
	  private List<Address> addresses = new ArrayList<>();  
	  
	  @ManyToMany  
	  @JoinTable(  
			  name = "user_tags",  
			  joinColumns = @JoinColumn(name = "user_id"),  
			  inverseJoinColumns = @JoinColumn(name = "tag_id")  
	  )  
	  @Builder.Default  
	  private Set<Tag> tags = new HashSet<>();  
	  
	  @OneToOne(mappedBy = "user")  
	  private Profile profile;  
	  
	  @ManyToMany  
	  @JoinTable(  
			  name = "wishlist",  
			  joinColumns = @JoinColumn(name = "user_id"),  
			  inverseJoinColumns = @JoinColumn(name = "product_id")  
	  )  
	  @Builder.Default  
	  private Set<Product> wishlist = new HashSet<>();  
	}
	```
- **View** - Defines how data is displayed. In tradition web apps, this is an HTML page generated using a template engine like **Thymeleaf**. (Below is an example of a view created using Thymeleaf)
	```html
	<!DOCTYPE html>  
	<html lang="en" xmlns:th="http://www.thymeleaf.org">  
		<head>  
			<meta charset="UTF-8">  
			<title>Online Store</title>  
		</head>  
		<body>  
			<h1 th:text="'Hello ' + ${name}"></h1>  
		</body>  
	</html>
	```
- **Controller** - Handles HTTP requests, processes data, and returns a response.

## Handling Requests in Spring MVC

Spring MVC provides different types of controllers to handle HTTP requests
- `@Controller` for returning HTML views (Below is an example of it, it shows also how you can pass data from the controller to the view)
	```java
	@Controller  
	public class HomeController {  
	  @RequestMapping("/")  
	  public String index(Model model) {  
	    model.addAttribute("name", "Brahim");  
	    return "index";  
	  }  
	}
	```
- `@RestController` for returning data. Spring MVC automatically convert Java objects to JSON objects. (Below is an example of how it works)
	```java
	@RestController  
	public class MessageController {  
	  @GetMapping("/messages")  
	  public Message[] getMessages() {  
	    return new Message[]{ new Message("Hello Brahim"), new Message("This is a test.") };  
	  }  
	  
	  @Getter  
	  @AllArgsConstructor  public static class Message {  
	    public String text;  
	  }  
	}
	```
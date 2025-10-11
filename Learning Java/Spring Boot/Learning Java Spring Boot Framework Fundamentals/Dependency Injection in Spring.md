
In this section, I explored Dependency Injection (DI), a core concept in Spring that helps manage object dependencies efficiently. I learned how Spring creates and injects objects, eliminating the need for manual object creation and improving code maintainability and test-ability.

## What is Dependency Injection

**Dependency Injection (DI)** is a pattern that allows objects to receive their dependencies from an external source rather than creating them internally.
DI makes applications more modular, testable, and maintainable by decoupling object creation from business logic.

## Ways to Inject Dependencies

There are multiple ways to inject dependencies in Spring
- **Constructor Injection (Recommended)** - Dependencies are passed through the class constructor and assigned to fields.
- **Setter Injection** - Dependencies are injected via setter methods after the object is created.  Useful when dependencies are optional or need to be changed at runtime.

## The Spring IoC Container

- **Inversion of Control (IoC) container** is responsible for managing the life-cycle of **Beans (Spring managed objects)**.
- When an application starts, the IoC container creates, configures, and injects dependencies into Beans automatically.
- Beans are stored in the **ApplicationContext**, allowing them to be retrieved and reused throughout the application

## Configuring Beans in Spring

There are two ways to configure beans in Spring
- **Using Annotations** - We can define beans using `@Component`, `@Service`, `@Repository`, and `@Controller`.
- **Programmatic-ally** - We can manually configure beans using Java-based configuration with `@Bean` inside a `@Configuration` class. This provides more fine-grained control over Bean creation.

When multiple Beans of the same type exist, we can specify which one to use with `@Primary` `@Qualifier`

## Lazy Initialization

By default, Spring eagerly initializes Beans when the application starts.
We can enable lazy initialization using `@Lazy`, which defers Bean creation until it is first needed, improving startup times in some cases.

## Bean Scopes

Spring Beans can have different scopes, determining how they are managed.
- **Singleton (default)** - A single instance is created and shared across the application.
- **Prototype** - A new instance is created each time it's requested.
- **Request, Session** and **Application** Scopes - Used in web applications to manage beans within HTTP request life-cycle.

## Bean Life-cycle Methods

Spring provides life-cycle hooks that allow us to execute code when a bean is created or destroyed.
We can define these methods using
- `@PostConstruct` - Executed after bean initialization.
- `@PreDestroy` - Executed before the bean is destroyed.
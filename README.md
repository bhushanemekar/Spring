# Spring
Spring Framework Basics
http://projects.spring.io/spring-framework/

Dependancy injections:

* Dependency Injection in JavaScript. 
	Dependency injection is a software design pattern that allows someone to remove hard-coded dependencies and makes it possible to change them. 
Dependencies can be injected to the object via 	
	the constructor 
	setter property
	defined method

* Dependency Injection
	-	A dependency is an object that can be used (a service).
	-	dependency injection is a technique whereby one object supplies the dependencies of another object.  
	-	An injection is the passing of a dependency to a dependent object (a client) that would use it.

explanation: there are two objects which are dependent on each other.
	DI is a way to decouple the dependencies.
	

	
Application COntext has some more functionality than bean factory.
event notification, AOP, 

Setting Properties:
	<bean 
		<property name="" value="">
		</bean>


Constructor injection:


	<bean id=" " class=" ">
		<constructor-arg type="" value="">
		<constructor-arg type="" value="" index="">
	</bean>

Reference Injection

	<bean 
		<property name="newName" ref="another id in spring.xml">
	</bean>
	
	
Inner Bean
	<bean>
		<property  name="var name given in class">
			<bean> // inner bean definition specifically for this bean class, no id needed
				<property name=" " value="..."/>
			</bean>
		</property>
	</bean>
	
	
Alias tag

	<alias name="old name/id" alias=" new given name/ alias">
	
	so ref tag can point to alias or id, 
	
	to make it point ID only we use <idRef tag
		<property name="zeroPoint">
			<idRef="pointZero"/>
		</property>
			
Representing collections in Spring.xml

	<bean ...>
		<property
			<list>
				<ref bean="zeroPoint"/>
			</list>
			
			
Bean Scopes:

	singleton
	prototype
	<bean scope="singleton/prototype"
	
	
	for web requests from JSP/servlet:
	request
	session
	global session (portlet context)
	
	
Bean inheritance
	<bean parent="some other bean id">
	
	for collections to inherit: merge ="true"
	</bean>
	
	
Autowired
		first: look for type
		2nd look for name same as attribute
		3rd you can add qualifier:
		
		@Qualifier("CircleQaulifier")
		setCentre()
	
		<bean>
			<qualifier value="CircleQaulifier">
			<prop> /
			
		</bean>

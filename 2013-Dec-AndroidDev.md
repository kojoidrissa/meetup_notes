#Test Driven Development
http://www.meetup.com/Houston-Android-Developers/events/152732192/

##What is TDD?
-  Helps you improve your code
-  Uses code to test your code
-  Tests can be automated and repeated
-  Makes refactoring easier

##TDD Lifecycle
1. Write your tests. They will fail
2. Write code to make your tests pass
3. REFACTOR!! Keep cleaning up while your tests pass

###Wny write tests first?
-  Forces you to think of how the class will work
-  Makes you consider the user of the code

##Testing Frameworks
-  JUnit is most common in Android

##Unit and Integration Testing
-  Divide your program into units and test them separately
-  Avoid the Singleton pattern
-  Isloate yourtests from external influences
    -  don't test code that's dependent on the network or database connectivity

##Mock and Fake Objects

##Interfaces
If all your objects implement simple interfaces, this makes testing easier

##Dependency Injection
Your objects shouldn't create the objects they depend on or reference global objects. But they should accept the interface for those objects in their constructors

##Concurrency
-  Keep your tests deterministic
-  If you require multiple threads to implement a test, make sure that every thread is finished before the main test method returns
-  If a background thread crashes or fails an assert after the main test method returns, it can attirbute the failure to some later test.

##Challenges
-  Learning curve: it takes time to learn; it's an "art", not a science
-  Ramp-up time: While you're learning, you'll be less productive
-  What to test? Learning to ID what parts need automated test
-  Migration: MOving a Non-TDD project TO TDD
-  UI testing is HARD!
    -  Calabash is a UI testing tool for Android

##Tools
-  Cucumber: BDD
-  


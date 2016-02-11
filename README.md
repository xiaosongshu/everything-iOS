##Table Of Contents

### Basic CS Knowledge / OOP / Algorithms
- [ ] Harvard CS50 courses on Youtube 
- [ ] Object Oriented Programming
- [ ] Algorithms

### [Frameworks and API] (https://github.com/xiaosongshu/everything-iOS/blob/master/README.md#frameworks-and-api-1)

- [ ] Properties
- [ ] App Life Cycle
- [ ] View Controller Life Cycle
- [ ] UIKit 
    - [ ] (UITableView, UIButton, UINavigationController, GestureRecognizers)
- [ ] Interface Builder 
    - [ ] (Storyboards, Segues, and the odd .xib)
- [ ] Foundation Types 
    - [ ] (NSArray, NSDictionary, NSString) and their Swift counterparts (Array, Dictionary and String)
- [ ] Networking
    - [ ] HTTP API (NSURLSession, Basic REST API concepts, JSON Parsing with NSJSONSerialization)
- [ ] Grand Central Dispatch 
    - [ ] (GCD, NSOperationQueue)
- [ ] Persistence 
    - [ ] (NSCoding, NSUserDefaults, CoreData)
- [ ] Memory Management 
    - [ ] (what Retain Cycles are and ARC fundamentals)
- [ ] Blocks
- [ ] Dependency Management
- [ ] CocoaPods

### [Development Patterns / Design Principles] (https://github.com/xiaosongshu/everything-iOS/blob/master/README.md#development-patterns--design-principles-1)

- [ ] Delegation 
    - [ ] (This is sort of the workhorse of most iOS API’s, you should DEFINITELY understand this)
- [ ] Model View Controller
    - [ ] (MVC, I don’t think Apple did the best job of encouraging best MVC separation, but it’s an important pattern that can help improve your code if you take the time to implement it properly. Also, it’s pretty much guaranteed to be on any iOS job interviewer’s question list.)
- [ ] Subclassing 
    - [ ] (Almost all user interface code will be a subclass of something.)
- [ ] Singleton 
    - [ ] (This one can definitely be abused… use sparingly.)

### [UX/UI] (https://github.com/xiaosongshu/everything-iOS/blob/master/README.md#uxui-1)

- [ ] Difference between mockups and wireframes

### [Tools] (https://github.com/xiaosongshu/everything-iOS/blob/master/README.md#tools-1)

- [ ] Git
- [ ] Analyze
- [ ] Instruments

### [Apple Submission] (https://github.com/xiaosongshu/everything-iOS/blob/master/README.md#apple-submission-1)

- [ ] Workflow

### Sources
- http://www.alloc-init.com/2016/01/how-to-become-a-developer-1/
- https://www.reddit.com/r/iOSProgramming/comments/3zeddx/quitting_my_job_to_polish_my_ios_coding_skills/cyowd3g
- http://cognitivedesign.com/papers/understanding-delegation-in-ios.html
- http://cognitivedesign.com/papers/understanding-blocks-in-ios.html

## Introduction to Computer Science
- [ ] [Harvard CS50 courses on Youtube] (https://www.youtube.com/playlist?list=PLhQjrBD2T383Xfn0zECHrOTpfOSlptPAB)

## Object Oriented Programming

#### Abstraction
- [ ] **Definition** 
    - [ ] The process of reducing objects to its essential characteristics. Used to reduce complexity and increase efficiency

#### Atomic vs Nonatomic
- [ ] **Definition** 
    - [ ] Atomic locks the object to prevent getter and setter to be called at the same time when more than one thread. Is default and has overhead.

#### Blocks
- [ ] **Definition** 
    - [ ] A chunk of code that can take arguments and return values. It can be passed as an argument if a method accepts blocks.

#### Category
- [ ] **Definition** 
    - [ ] Allows you to add new methods to a class

#### Class
- [ ] **Definition** 
    - [ ] Encapsulates a logical structure with properties and methods

#### Completion Handler
- [ ] **Definition** 
    - [ ] Block declaration passed as a parameter. Gets called after a task is executed.

#### Constructor
- [ ] **Definition** 
    - [ ] Used to instantiate a class, optionally with properties.

#### Delegate
- [ ] **Definition** 
    - [ ] Allows one object to act in behalf, or in coordination, with another

#### Encapsulation
- [ ] **Definition**
    - [ ] Hiding details of an object from everything else

#### enum
- [ ] **Definition** 
    - [x] Lets you define a set of constants. 
- [ ] Use typedef to not have to use “enum” all the time.
    - [x] A **typedef** creates an alias, or alternative name, for an existing type that the compiler will recognize as being the same as that type. Normally the syntax for a typedef is this: `typedef [existingtypename] [newalias];`
    - [x] Thus, if we want "count_raccoons" to be an alias for a C integer type, we would use the following: `typedef int count_raccoons;`
    - [x] However, the syntax for a typedef that involves blocks is different. A typedef for a block uses syntax designed for what is known in C as a function pointer, which is: `typedef [returntype] [newalias] [argumenttype(s)];`
    - [x] `typedef void (^ChooseYesOrNoCallbackBlock) (BOOL);` This says that a new alias ChooseYesOrNoCallbackBlock is defined for a block that does not return a value, and accepts a single parameter of type Boolean. Once this typedef is included, we can refer to the block as just ChooseYesOrNoCallbackBlock in both the property and method declarations.

#### Enumeration
- [ ] **Definition** 
    - [ ] A complete, ordered listing of all items in a collection.

#### Exception Handling
- [ ] **Definition** 
    - [ ] Trapping errors in code so the program doesn’t crash

#### Grand Central Dispatch
- [ ] **Definition** 
    - [ ] Provides support for concurrent code

#### Heap (Memory)
- [ ] **Definition** 
    - [ ] A buffer is a chunk of memory that comes from the heap. You can store something like text in it and use it in multiple functions. Once the buffer is no longer needed, it’s released back to the heap.

#### Inheritance
- [ ] **Definition** 
    - [ ] When a class is based on another class, it inherits characteristics from it.

#### Introspection
- [ ] **Definition** 
    - [ ] Allows us to learn certain things from an object at runtime. Ex: are you of this class? do you respond to this method?

#### Key-Value Coding
- [ ] **Definition** 
    - [ ] Allows you to access a property of an object using a string

#### Key-Value Observing
- [ ] **Definition** 
    - [ ] Allows you to observe for changes in a property

#### Loose Coupling
- [ ] **Definition** 
    - [ ] When objects are independent from each other and don’t change the state of other objects

#### Manual Retain Release (MRR)
- [ ] **Definition** 
    - [ ] Manually control objects’ reference count. You need to claim and release objects.
- [ ] **Use-cases**
    - [ ] *alloc* - create object and claim ownership of it
    - [ ] *retain* - claim ownership of existing object
    - [ ] *release* - relinquish ownership and immediately destroy object
    - [ ] *autorelease* - relinquish ownership of object, but defer it’s destruction
    - [ ] *autoreleasepool* - makes sure autoreleased objects are destroyed

#### Method Swizzling
- [ ] **Definition** 
    - [ ] Adding a method or exchanging 2 at runtime

#### Pass by reference
- [ ] **Definition** 
    - [ ] Instead of creating a copy of a value, you send the original value. Changes are global.

#### Pointer
- [ ] **Definition** 
    - [ ] Memory location of a value

#### Polymorphism
- [ ] **Definition** 
    - [ ] Meaning multiple shapes, where one or more classes can inherit from the same parent class but implement different methods.

#### Protocols

- [ ] **Definition**
    - [x]  Protocols are groups of related properties and methods that can be implemented by any class (list of methods that a delegate must or may implemented to get messages from a delegating object)

- [ ] **Notes**
    - [x] Another way to look at a protocol is by use of the term that is used in Java and C++ for the same idea, which is interface. A protocol specifies the interface between the delegating object and the delegate object.
    - [x] Note that Objective-C is a single-inheritance language--a class (and thus its objects) can only inherit from a single superclass. Delegation provides a little of what multiple inheritance languages have by allowing inheritance from something other than the superclass of a class.
    - [x] Protocols can also conform to a protocol
    - [x] The next line in the protocol lists a single delegate method. I could have put a line above it, @required, to indicate that it is a required method. This would mean that the delegate object, to conform to the protocol, MUST implement the method. I did not actually have to do that because @required is the default. If the method is optional, that can be indicated by using the directive @optional. When a @required or @optional directive is included, this says that all methods listed after that directive are specified as indicated until the opposite directive is encountered. @end, obviously, indicates the end of the definition of the protocol.

#### Serialization
- [ ] **Definition** 
    - [ ] Serialization** - process of converting objects to files and back again

#### Singleton 
- [ ] **Definition** 
    - [ ] A design pattern that ensures only one instance of a class exists, and that there’s access to it globally (NSUserDefaults, UIApplication, UIScreen, NSFileManager).

#### Stack (Memory)
- [ ] **Definition** 
    - [ ] Where the frame of functions are stored. When a function is called, its frame is pushed onto the top of the stack. When the function finishes, its frame is removed from the top.

## Algorithms
- [ ] https://docs.google.com/document/d/1lOelviSSEf7kLbPxKRAfZ-dac4-Lj_kzyPsNGprYs48/edit?ts=56b40d14

## Frameworks and API

#### App Life Cycle
- [ ] **UIApplication Object** - manages event loop and other high level app behaviors. Do not subclass.
- [ ] **App Delegate Object** - works with UIApplication Object to handle app initialization, state transitions, and high level app events.
- [ ] **Main Run Loop** - processes all user-related events on the main thread.
- [ ] States of App
    - [ ] **Not Running** - app has not launched or was terminated.
    - [ ] **Inactive** - app is running in the foreground but not receiving events. (get a text while using app)
    - [ ] **Active** - app is running in foreground and receiving events
    - [ ] **Background** - app is in background and executing code for a period time. Time can be extended if needed.
    - [ ] **Suspended** - App is in the background and not executing code.

#### View Controller Life Cycle
- [ ] Allocation and Initialization of View Controller
    - [ ] **loadView** - creates the view controller (only when view controller is created programmatically).
    - [ ] **initWithNibName** - using xib files
    - [ ] **initWithCoder** - using storyboards
- [ ] **viewDidLoad** - called when view is loaded into memory (only called once). Bounds not final.
    - [ ] Good to init and set up objects
- [ ] **viewWillAppear** - when the view is about to appear on screen (called multiple times). Bounds defined.
- [ ] **viewDidAppear** - view has been displayed and added to the view hierarchy
- [ ] **viewWillDisappear** - clean code and do any saving
- [ ] **viewDidDisappear** - clean code and do any saving
- [ ] **viewWillLayoutSubviews** - about to layout subviews (any time frame changes. First step when bounds are final.
- [ ] **viewDidLayoutSubviews** - subviews laid out.

#### UIKit (UITableView, UIButton, UINavigationController, GestureRecognizers)

#### Interface Builder (Storyboards, Segues, and the odd .xib)

#### Foundation Types (NSArray, NSDictionary, NSString) and their Swift counterparts (Array, Dictionary and String)
#### Networking: HTTP API (NSURLSession, Basic REST API concepts, JSON Parsing with NSJSONSerialization)
- [ ] **AFNetworking** - Block based networking library, so easy to use and so powerful.

#### Grand Central Dispatch (GCD, NSOperationQueue)
- [ ] GCD
- [ ] Don’t forgot to switch back to the main thread before doing anything with the UI
- [ ] Good explanation of GCD, including making your own queues: http://www.fieryrobot.com/blog/2010/06/27/a-simple-job-queue-with-grand-central-dispatch/
```
dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0), ^(void) {
    // Your code
        dispatch_async(dispatch_get_main_queue(), ^(void) {
        // Now you can interact with the UI
        });
});
```

#### Persistence (NSCoding, NSUserDefaults, CoreData)
- [ ] **NSCoding**
- [ ] **NSUserDefaults**
- [ ] **Core Data**
    - [ ] What is it? - framework that manages an object graph. Used to store data into an Sqlite file.
    - [ ] **Core Data Stack** - includes managed object model, persistent store coordinator, and one or more managed object contexts
    - [ ] **Managed Object Model**  - The data model that contains information about the models or entities of the object graph, what attributes they have, and how they relate to one another
    - [ ] **Persistent Store Coordinator**  - persist data to disk and makes sure persistent store and data model are compatible. Takes care of loading, saving, and caching.
    - [ ] **Managed Object Context**  - manages a collection of model objects, instances of NSManagegedObject, and keeps a reference to a persistent store coordinator
    - [ ] **NSManagedObject**  - a record in Core Data’s backing store (like a row in a database table)
        - [ ] **NSEntityDescription**  - includes information about managed object (entity, attributes, relationships)
    - [ ] **NSFetchedResultsController**  - class that helps keep core data and the user interface synchronized through notifications posted by the managed object context
    - [ ] **Managed Object**  - the objects that store data. For each new record, a new managed object is created to store the data.
    - [ ] **Persistence Store Coordinator**  - central object that hold a reference to a managed object model. Never access it directly
    - [ ] **Managed Object Context**  - maintains status of objects in relation to data store and manages relationships between managed objects defined by the managed object model.

#### Memory Management (what Retain Cycles are and ARC fundamentals)
- [ ] **Definition** 
    - [ ] Automatic Reference Counting (ARC) demanages object ownership automatically
- [ ] **Properties**
    - [ ] *Strong Property (default)* - creates owning relationship
    - [x]  *Weak Propperty (default)* - creates owning relationship
    - [x]  *Weak Property* - relationship without ownership 
    - [ ] *Copy* - Creates copy and takes ownership of that. Will freeze the object at the value given.
    - [ ] *Retain Cycle* - form of memory leak where two objects own each other and neither are destroyed
    - [ ] *Dangling Pointer* - points to an object that no longer exists.
    - [ ] *Unsafe_unretained* - similar to weak, doesn’t set value to nil if reference is destroyed. Should only be used when weak isn’t supported
    - [x] *Assign* - has nothing to do with memory management. Used to be a way to implement weak properties, should not be used anymore.
erty** - relationship without ownership 
    - [ ] *Copy* - Creates copy and takes ownership of that. Will freeze the object at the value given.
    - [ ] *Retain Cycle* - form of memory leak where two objects own each other and neither are destroyed
    - [ ] *Dangling Pointer* - points to an object that no longer exists.
    - [ ] *Unsafe_unretained* - similar to weak, doesn’t set value to nil if reference is destroyed. Should only be used when weak isn’t supported
    - [x] *Assign* - has nothing to do with memory management. Used to be a way to implement weak properties, should not be used anymore.

#### Blocks
- [ ] **Definition**
    - [x] A block, in its simplest form, is a piece of code that begins with a carat character and is surrounded by curly braces, as seen below:
```^ {
    / / This is a block
     }```
    - [x] A block is not only a piece of code, but it can be assigned to a variable.
- [ ] **Use-cases**
    - [x] Blocks are frequently used in iOS API calls to pass an entire piece of code, rather than just a value, as a parameter. For example, they are used in animation APIs to define aspects of a target view that the system will end up displaying when the animation has been completed. In Grand Central Dispatch, code packaged as a block can be put into a queue and executed, say on a background thread.
	- [x] Blocks can also be used in callbacks that occur as a result of events, much like delegates are. In some cases, blocks are arguably simpler to use delegation, and are preferred by many programmers.

- [ ] **Notes**
    - [ ] There is a great tutorial on blocks **here??**. There are still times when delegates/protocols or NSNotifications make sense, but blocks should be your first consideration.
    - [ ] Beware of retain cycles with blocks. Check out this link http://zearfoss.wordpress.com/2012/05/11/a-quick-gotcha-about-blocks/

#### Dependency Management
#### CocoaPods

## Development Patterns / Design Principles

#### Delegation
- [ ] **Definition**
    - [x] A delegate is an object that acts on behalf of, or in coordination with, another object when that object encounters an event in a program
- [ ] **Usecases**
    1. *calback mechanism : UIAlertView*
        - [x] Delegation is used when dealing with events, and in its simplest form, it is just a callback mechanism: A program can start something up, and then go on to do other things. If and when there is a response to what was started up, it comes in the form of a message that causes the execution of a method that can then deal with the response. Even if the program starts something up but then does nothing but wait, it is a convenient way to organize things. 
        - [x] The important idea here is that delegation allowed you to set up an off-the-shelf object--an instance of UIAlertView--that as the result of an event (user tapping a button) calls a method of the object that set it up so that you can do what you like with the result of the event 
        - [x] `((void)alertView:(UIAlertView *)alertView clickedButtonAtIndex:(NSInteger)buttonIndex)`
    2. *complex APIs that allow more subtle customization of UI Elements : UITableViews*
    	- [x] number of rows & numer of sections is part of UITableViewDataSource Protocol rather than UITableViewDelegate Protocol
    	- [x] This shows an example of a common thing that is done in delegate methods. It is basically setting a parameter for use by the delegating object, and, when necessary, using information that is passed to it by the delegating object. This is quite different from the simple callback, where information is passed only from the delegating object to the delegate.
    	- [x] The method for providing data is tableView:cellForRowAtIndexPath
    	- [x] Very few of the methods associated with a table view are required. Of the 32 methods defined as delegate methods, none are required. Of the 11 methods defined as data source methods, only 2 are required (now of rows and the data for a row).

    3. *communicate between different objects in the app : info passed from a child object to its parent*
    	- [x] The main difference here from UIAlertView is that this is not an off-the-shelf object from the iOS API, but a custom object, with a custom protocol and custom delegate method, that was created from scratch.


- [ ] **Who's the Delegate?**
    - [x] The helper object you are using is, very often, the delegating object, and in such a case your program would be the delegate object, also known as just the delegate. This is often the case for the helper objects that are part of the iOS API.
    - [x] The UIAlertView object is the delegating object, as is common with the iOS API objects, and, as suggested when delegate was set to "self", the object that set this up, MainViewController, is the delegate (object).

#### MVC - Model (Data), View (UI), Controller (Gateway)

#### Subclassing

#### Singleton - design pattern where you declare and use a single instance of an object
```
Carrying on with GCD, dispatch_once is really useful:
    + (MyClass *)sharedClass {
static MyClass *_shared = nil;
static dispatch_once_t onceToken;
dispatch_once(&onceToken, ^{
    _shared = [[MyClass alloc] init];
}); 
return _shared;
}
```

You'll be doing this a bit, especially when you see how costly it is to create things like NSDateFormatter many times.
- [ ] **Target-Action** - One object send message to another object when event occurs

## UX/UI
- [ ] Difference between mockups and wireframes

##  Tools

#### Git

#### Analyze
- [ ] **Product** -> Analyze can pick up a lot of potential issues (and a lot of red herrings).

#### Instruments
- 	[ ] **Profiling** - provides insight into which parts of the code are used most often.
- [ ] **Time Profiler** - let’s you see how much time you’re spending in each method and which one consumes the most.
- [ ] **Allocations** - shows you details on all objects created and the memory that backs them.
- [ ] **Leaks** - remembers all objects allocated and periodically checks if they’re still referenced

## Apple Submission

#### Workflow
- [ ] Create Certificate (Development + Distribution)
- [ ] Register Devices - need UDID
- [ ] Register App ID - each app needs one
- [ ] Create Provisioning and Distribution profiles - authorizes app to use certain apple services and ensures you are the one submitting the app
- [ ] Archive
- [ ] Submit to iTunes Connect
- [ ] Prepare iTunes Connect app and submit.

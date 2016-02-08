# everything-iOS

#### Basic CS Knowledge / OOP

- [ ] Harvard CS50 courses on Youtube
- [ ] Object Oriented Programming
- [ ] Algorithms

#### Frameworks and API

- [ ] Properties
- [ ] App Life Cycle
- [ ] View Controller Life Cycle
- [ ] UIKit (UITableView, UIButton, UINavigationController, GestureRecognizers)
- [ ] Interface Builder (Storyboards, Segues, and the odd .xib)
- [ ] Foundation Types (NSArray, NSDictionary, NSString) and their Swift counterparts (Array, Dictionary and String)
- [ ] Networking: HTTP API (NSURLSession, Basic REST API concepts, JSON Parsing with NSJSONSerialization)
- [ ] Grand Central Dispatch (GCD, NSOperationQueue)
- [ ] Persistence (NSCoding, NSUserDefaults, CoreData)
- [ ] Memory Management (what Retain Cycles are and ARC fundamentals)
- [ ] Blocks
- [ ] Dependency Management
    - [ ] CocoaPods

#### Development Patterns / Design Principles

- [ ] Delegation (This is sort of the workhorse of most iOS API’s, you should DEFINITELY understand this)
- [ ] Model View Controller (MVC, I don’t think Apple did the best job of encouraging best MVC separation, but it’s an important pattern that can help improve your code if you take the time to implement it properly. Also, it’s pretty much guaranteed to be on any iOS job interviewer’s question list.)
- [ ] Subclassing (Almost all user interface code will be a subclass of something.)
- [ ] Singleton (This one can definitely be abused… use sparingly.)

#### UX/UI

- [ ] Difference between mockups and wireframes

#### Tools

- [ ] Git
- [ ] Analyze
- [ ] Instruments

#### Apple Submission

- [ ] Workflow

#### Sources
- http://www.alloc-init.com/2016/01/how-to-become-a-developer-1/
- https://www.reddit.com/r/iOSProgramming/comments/3zeddx/quitting_my_job_to_polish_my_ios_coding_skills/cyowd3g
 
# Basic CS Knowledge / OOP

- Harvard CS50 courses on Youtube

- [ ] Object Oriented Programming

    - [ ] Abstraction - the process of reducing objects to its essential characteristics. Used to reduce complexity and increase efficiency

    - [ ] Automatic Reference Counting (ARC) - manages object ownership automatically

    - [ ] Atomic vs Nonatomic - Atomic locks the object to prevent getter and setter to be called at the same time when more than one thread. Is default and has overhead.

    - [ ] Blocks - a chunk of code that can take arguments and return values. It can be passed as an argument if a method accepts blocks.

    - [ ] Category - allows you to add new methods to a class

    - [ ] Class - encapsulates a logical structure with properties and methods

    - [ ] Completion Handler - block declaration passed as a parameter. Gets called after a task is executed.

    - [ ] Constructor - used to instantiate a class, optionally with properties.

    - [ ] Delegate - Allows one object to act in behalf, or in coordination, with another

    - [ ] Encapsulation - hiding details of an object from everything else

    - [ ] enum - Lets you define a set of constants. Use typedef to not have to use “enum” all the time.

    - [ ] Enumeration - a complete, ordered listing of all items in a collection.

    - [ ] Exception Handling - trapping errors in code so the program doesn’t crash

    - [ ] Grand Central Dispatch - provides support for concurrent code

    - [ ] Heap (Memory) - a buffer is a chunk of memory that comes from the heap. You can store something like text in it and use it in multiple functions. Once the buffer is no longer needed, it’s released back to the heap.

    - [ ] Inheritance - when a class is based on another class, it inherits characteristics from it.

    - [ ] Introspection - allows us to learn certain things from an object at runtime. Ex: are you of this class? do you respond to this method?

    - [ ] Key-Value Coding - allows you to access a property of an object using a string

    - [ ] Key-Value Observing - allows you to observe for changes in a property

    - [ ] Loose Coupling - when objects are independent from each other and don’t change the state of other objects

    - [ ] Manual Retain Release (MRR) - Manually control objects’ reference count. You need to claim and release objects.

        - [ ] alloc - create object and claim ownership of it

        - [ ] retain - claim ownership of existing object

        - [ ] release - relinquish ownership and immediately destroy object

        - [ ] autorelease - relinquish ownership of object, but defer it’s destruction

        - [ ] autoreleasepool - makes sure autoreleased objects are destroyed

    - [ ] Method Swizzling - adding a method or exchanging 2 at runtime

    - [ ] Pass by reference - instead of creating a copy of a value, you send the original value. Changes are global.

    - [ ] Pointer - memory location of a value

    - [ ] Polymorphism - meaning multiple shapes, where one or more classes can inherit from the same parent class but implement different methods.

    - [ ] Protocols - groups of related properties and methods that can be implemented by any class

    - [ ] Serialization - process of converting objects to files and back again

    - [ ] Singleton - a design pattern that ensures only one instance of a class exists, and that there’s access to it globally (NSUserDefaults, UIApplication, UIScreen, NSFileManager).

    - [ ] Stack (Memory) - where the frame of functions are stored. When a function is called, its frame is pushed onto the top of the stack. When the function finishes, its frame is removed from the top.

- [ ] Algorithms

    - [ ] https://docs.google.com/document/d/1lOelviSSEf7kLbPxKRAfZ-dac4-Lj_kzyPsNGprYs48/edit?ts=56b40d14





# Development Patterns / Design Principles

- [ ] Delegation - one object acts on behalf of, or in coordination with, another object

- [ ] MVC - Model (Data), View (UI), Controller (Gateway)

- [ ] Subclassing -----

- [ ] Singleton - design pattern where you declare and use a single instance of an object

    - [ ]
Carrying on with GCD, dispatch_once is really useful:
    + (MyClass *)sharedClass {
static MyClass *_shared = nil;
static dispatch_once_t onceToken;
dispatch_once(&onceToken, ^{
    _shared = [[MyClass alloc] init];
}); 
return _shared;
}


You'll be doing this a bit, especially when you see how costly it is to create things like NSDateFormatter many times.

- [ ] Target-Action - One object send message to another object when event occurs

# Frameworks and API

- [ ] Properties

    - [ ] Strong Property (default) - creates owning relationship

    - [ ] Weak Property - relationship without ownership

    - [ ] Copy - Creates copy and takes ownership of that. Will freeze the object at the value given.

    - [ ] Retain Cycle - form of memory leak where two objects own each other and neither are destroyed

    - [ ] Dangling Pointer - points to an object that no longer exists.

    - [ ] Unsafe_unretained - similar to weak, doesn’t set value to nil if reference is destroyed. Should only be used when weak isn’t supported

    - [ ] Assign - has nothing to do with memory management. Used to be a way to implement weak properties, should not be used anymore.

- [ ] App Life Cycle

    - [ ] UIApplication Object - manages event loop and other high level app behaviors. Do not subclass.

    - [ ] App Delegate Object - works with UIApplication Object to handle app initialization, state transitions, and high level app events.

    - [ ] Main Run Loop - processes all user-related events on the main thread.

    - [ ] States of App

        - [ ] Not Running - app has not launched or was terminated.

        - [ ] Inactive - app is running in the foreground but not receiving events. (get a text while using app)

        - [ ] Active - app is running in foreground and receiving events

        - [ ] Background - app is in background and executing code for a period time. Time can be extended if needed.

        - [ ] Suspended - App is in the background and not executing code.

- [ ] View Controller Life Cycle

    - [ ] Allocation and Initialization of View Controller

        - [ ] loadView - creates the view controller (only when view controller is created programmatically).

        - [ ] initWithNibName - using xib files

        - [ ] initWithCoder - using storyboards

    - [ ] viewDidLoad - called when view is loaded into memory (only called once). Bounds not final.

        - [ ] Good to init and set up objects

    - [ ] viewWillAppear - when the view is about to appear on screen (called multiple times). Bounds defined.

    - [ ] viewDidAppear - view has been displayed and added to the view hierarchy

    - [ ] viewWillDisappear - clean code and do any saving

    - [ ] viewDidDisappear - clean code and do any saving

    - [ ] viewWillLayoutSubviews - about to layout subviews (any time frame changes. First step when bounds are final.

    - [ ] viewDidLayoutSubviews - subviews laid out.

- [ ] UIKit (UITableView, UIButton, UINavigationController, GestureRecognizers)

- [ ] Interface Builder (Storyboards, Segues, and the odd .xib)

- [ ] Foundation Types (NSArray, NSDictionary, NSString) and their Swift counterparts (Array, Dictionary and String)

- [ ] Networking: HTTP API (NSURLSession, Basic REST API concepts, JSON Parsing with NSJSONSerialization)

    - [ ] AFNetworking - Block based networking library, so easy to use and so powerful.

- [ ] Grand Central Dispatch (GCD, NSOperationQueue)

    - [ ] GCD

        - [ ] dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0),
        -    ^(void) {
       // Your code
      dispatch_async(dispatch_get_main_queue(), ^(void) {
         // Now you can interact with the UI
      });
});

        - [ ] Don’t forgot to switch back to the main thread before doing anything with the UI

        - [ ] Good explanation of GCD, including making your own queues, http://www.fieryrobot.com/blog/2010/06/27/a-simple-job-queue-with-grand-central-dispatch/

- [ ] Persistence (NSCoding, NSUserDefaults, CoreData)

    - [ ] NSCoding

    - [ ] NSUserDefaults

    - [ ] Core Data

        - [ ] What is it? - framework that manages an object graph. Used to store data into an Sqlite file.

        - [ ] Core Data Stack - includes managed object model, persistent store coordinator, and one or more managed object contexts

        - [ ] Managed Object Model - The data model that contains information about the models or entities of the object graph, what attributes they have, and how they relate to one another

        - [ ] Persistent Store Coordinator - persist data to disk and makes sure persistent store and data model are compatible. Takes care of loading, saving, and caching.

        - [ ] Managed Object Context - manages a collection of model objects, instances of NSManagegedObject, and keeps a reference to a persistent store coordinator

        - [ ] NSManagedObject - a record in Core Data’s backing store (like a row in a database table)

            - [ ] NSEntityDescription - includes information about managed object (entity, attributes, relationships)

        - [ ] NSFetchedResultsController - class that helps keep core data and the user interface synchronized through notifications posted by the managed object context

        - [ ] Managed Object - the objects that store data. For each new record, a new managed object is created to store the data.

        - [ ] Persistence Store Coordinator - central object that hold a reference to a managed object model. Never access it directly

        - [ ] Managed Object Context - maintains status of objects in relation to data store and manages relationships between managed objects defined by the managed object model.

- [ ] Memory Management (what Retain Cycles are and ARC fundamentals)

- [ ] Blocks

    - [ ] There is a great tutorial on blocks here. There are still times when delegates/protocols or NSNotifications make sense, but blocks should be your first consideration.

    - [ ] Beware of retain cycles with blocks. Check out this link http://zearfoss.wordpress.com/2012/05/11/a-quick-gotcha-about-blocks/
- Dependency Management
    - CocoaPods


# Tools

- [ ] Git

- [ ] Analyze

    - [ ] Product -> Analyze can pick up a lot of potential issues (and a lot of red herrings).

- [ ] Instruments

    - [ ] Profiling - provides insight into which parts of the code are used most often.

    - [ ] Time Profiler - let’s you see how much time you’re spending in each method and which one consumes the most.

    - [ ] Allocations - shows you details on all objects created and the memory that backs them.

    - [ ] Leaks - remembers all objects allocated and periodically checks if they’re still referenced

# Apple Submission

- Workflow

    - Create Certificate (Development + Distribution)
    - Register Devices - need UDID
    - Register App ID - each app needs one
    - Create Provisioning and Distribution profiles - authorizes app to use certain apple services and ensures you are the one submitting the app
    - Archive
    - Submit to iTunes Connect
    - Prepare iTunes Connect app and submit.

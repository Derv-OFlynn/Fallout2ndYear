 #ExamPrep #SWE2 

# <mark style="background: #69E7E4;">02. Business Modelling</mark>

Early Phase of Development

<mark style="background:#69E7E4;">Inputs:</mark>
- Informal Specification
	
<mark style="background:#69E7E4;">Activities:</mark>
- Create use case model
- Define use cases
- Create domain model
- Create Glossary
    
### <mark style="background:#69E7E4;">Restaurant System (Example):</mark>

Current System uses physical booking sheets

<mark style="background:#69E7E4;">Current Functionality:</mark>

Advance bookings are recorded on sheets
- Name and phone number of contact
- Number of diners: ("covers")
	
'Walk-ins' also recorded:
- Number of covers only
 
 Bookings allocated to a table
Cancellations, etc., are recorded physically on the booking sheet	

### <mark style="background:#69E7E4;">Define First Iteration:</mark>

First iteration should implement the minimal useful system

<mark style="background:#69E7E4;">Basic functionality:</mark>
- Record bookings
- Update booking sheet information

System could then replace manual sheets

### <mark style="background:#69E7E4;">Use Case view:</mark>

This view is intended to provide a structured view of the system's functionality

Based round a description of how users interact with the system

Supported by UML use case diagrams

Serves as the starting point for all subsequent development

### <mark style="background: #69E7E4;">Use Cases:</mark> 
The different tasks that users can perform while interacting with the system

<mark style="background: #69E7E4;">Preliminary list for booking system:</mark>
1. record information about a new booking
2. cancel a booking
3. record the arrival of a customer
4. move a customer from one table to another

### <mark style="background:#69E7E4;">Actors:</mark>

Actors are the roles users play when interacting with a system, e.g.:
- Receptionist (makes bookings)
- Head waiter (assigns tables etc.)

Individual users may play one or more role at different times

Customers are not users of the system, hence not recorded as an actor

### <mark style="background:#69E7E4;">Use Case Diagrams:</mark>

Show use cases, actors and who does what

![](https://i.imgur.com/846Btdk.png)


### <mark style="background:#69E7E4;">Describing Use Cases:</mark>

A use case comprises all the possible interactions that a user can have when performing a given task

These are described as <mark style="background: #69E7E4;">courses of events</mark>, or <mark style="background: #69E7E4;">scenarios</mark>

A full description of a use case includes:
- a <mark style="background: #69E7E4;">basic</mark> course of events
- an number of alternative and exceptional courses

### <mark style="background:#69E7E4;">Basic Course of Events:</mark>

This describes what happens in the ‘normal’ case

For example, for ‘Record Booking’:
1. receptionist enters date
2. system displays bookings
3. receptionist enters details
4. system records and displays new booking

Often a dialogue between system and user

### <mark style="background:#69E7E4;">Alternative course of events:</mark>

- Describe predicted alternative flows
- For example, if no table is available:
	1. receptionist enters date
	2. system displays bookings
	3. no table available: end of use case
	
    
### <mark style="background:#69E7E4;">Exceptional Courses of Events:</mark>

Situations where a mistake has been made

E.g. allocate a booking to a small table
1.  receptionist enters date
2.  system displays bookings
3. receptionist enters details
4. system asks for confirmation of oversize booking
5. if “no”, use case terminates with no booking made
6. if “yes”, booking recorded with warning flag
	

### <mark style="background:#69E7E4;">Use case templates:</mark>

UML does not define a standard format for use case descriptions

Various <mark style="background: #69E7E4;">templates</mark> have been defined to structure descriptions

Essentially a list of subheadings such as:
- name
- actors
- courses of events
	
    
### <mark style="background:#69E7E4;">User-interface Prototype:</mark>

When writing use cases, it is useful to have a rough idea of the planned user interface

 ![](https://i.imgur.com/SwppFVl.png)


### <mark style="background:#69E7E4;">Shared Functionality:</mark>

Different use cases can overlap

E.g. ‘Record Arrival’:
- head waiter enters date
- system displays bookings
- head waiter confirms arrival for booking
- system records this and updates display

First two steps shared with ‘Record Booking’ (even though different actor)

### <mark style="background:#69E7E4;">Use Case Inclusion:</mark>

Move shared functionality to a separate use case, eg ‘Display Bookings’:
1. user enters a date
2. system displays bookings for that date

Include this in other use cases:
1. receptionist performs ‘Display Bookings’
2. receptionist enters details
3. system records and displays new booking    

### <mark style="background:#69E7E4;">The 'include' Dependency:</mark>

UML shows inclusion as a dependency between use cases, labelled with the stereotype include:
![](https://i.imgur.com/PNJcFKh.png)


### <mark style="background:#69E7E4;">Actor Generalisation:</mark>

This diagram shows that the receptionist can display bookings without performing the including use case ‘Record Booking’

Head waiters can also display bookings

Introduce a more general actor to show what the other two actors have in common

The initial actors are <mark style="background: #69E7E4;">specialisations</mark> of the general actor

![](https://i.imgur.com/gTDD7TP.png)

### <mark style="background:#69E7E4;">Use Case Extension:</mark>

Recording a walk-in can be described as an exceptional source of events: someone arrives but there’s no booking recorded

It could also be a separate use case: A customer arrives and asks if there's a free table

Then it can extend ‘Record Arrival’. Even without a booking, the customer stays to eat

### <mark style="background: #69E7E4;">The 'extend' Dependency:</mark>

Use case extension is shown with a dependency

![](https://i.imgur.com/kOtqske.png)

### <mark style="background:#69E7E4;">Complete Use-Case Diagram:</mark>

![](https://i.imgur.com/z5Z9KwB.png)

### <mark style="background:#69E7E4;">Domain Modelling:</mark>
    
Using UML to construct a model of the real-world system - similar to entity-relationship modelling
        
Model recorded as a class diagram

<mark style="background: #69E7E4;">‘Seamless development’: </mark> 
- same notation used for analysis and design
- design can evolve from initial domain model

  
### <mark style="background:#69E7E4;">Domain Model Notation:</mark>

Subset of class diagram notation
- <mark style="background:#69E7E4;">classes</mark> represent real-world entities
- <mark style="background:#69E7E4;">associations</mark> represent relationships between the entities
- <mark style="background:#69E7E4;">attributes</mark> represent the data held about entities
- <mark style="background:#69E7E4;">generalisation</mark> can be used to simplify the structure of the model
	

### <mark style="background:#69E7E4;">Customers and Reservations:</mark>

Basic business fact: customers make reservations

![](https://i.imgur.com/c1veJJB.png)

### <mark style="background:#69E7E4;">Defining a Relationships:</mark>

Give a name to the relationship
- use a verb so that the relationship can be read as a sentence
	
A customer can make many reservations

How many people make a reservation?
- one principal contact whose details are held
- the expected number of diners can be modelled as an attribute of the reservation


### <mark style="background:#69E7E4;">Tables:</mark>

Is table number an attribute of ‘Reservation’?

Better modelled as a separate class
- tables exist even if there are no reservations
- other attributes of tables, e.g. size, can be stored

![](https://i.imgur.com/YrICZbE.png)

### <mark style="background:#69E7E4;">Constraints:</mark>

Not all domain properties can be shown graphically e.g. it should be impossible to double-book a table

<mark style="background: #69E7E4;">Constraints</mark> add information to models: Written in a note connected to the model element being constrained
    
### <mark style="background:#69E7E4;">Use of Generalisation:</mark>

A superclass can be used to show the properties shared by different types of booking

![](https://i.imgur.com/Ou4D29Z.png)

### <mark style="background:#69E7E4;">Correctness:</mark>

How do we know when a domain model is complete? We don't: there are lots of plausible models in most cases

Domain modelling is not an end in itself, but a guide to further development

Realizing use cases tests the domain model, and will usually lead to refinements

### <mark style="background:#69E7E4;">Glossaries:</mark>

- Domain models capture important system concepts
- Useful to record these terms and their definitions for use throughout a project
- Do this in the form of a <mark style="background: #69E7E4;">glossary</mark>

### <mark style="background:#69E7E4;">Partial restaurant glossary:</mark>

- <mark style="background:#69E7E4;">Booking:</mark> an assignment of diners to a table
- <mark style="background:#69E7E4;">Covers:</mark> the number of diners for a booking
- <mark style="background:#69E7E4;">Customer:</mark> a person who makes a reservation
- <mark style="background:#69E7E4;">Reservation:</mark> a booking made in advance
- <mark style="background:#69E7E4;">Walk-in:</mark> a booking that is not made in advance

# <mark style="background: #69E7E4;">03. Analysis Modelling - Practical OO Design</mark>

### <mark style="background:#69E7E4;">Analysis:</mark>

What is to be analysed? The system requirements

Why? To demonstrate their implementability

How? By drawing interaction diagrams realising use cases

<mark style="background:#69E7E4;">From Requirements get:</mark>
- Use-case descriptions which document external interactions with the putative software, known as external messages between actor and system
- Domain Model which defines the relationships between important business concepts

Analysis is about finding out how objects derived from the domain model can be made to cooperate in such a way as to implement behaviour described in use-cases

Hence the term, "use-case realisation"

### <mark style="background:#69E7E4;">Analysis and UP:</mark>

Analysis in the UP mostly occurs in the Elaboration Phase

Use-case realisation leads to a more comprehensive class diagram, usually a reified version of the domain model

Besides use-case realisations, another important product of the analysis workflow is the <mark style="background: #69E7E4;">Software Architecture Description (SAD)</mark>

### <mark style="background:#69E7E4;">Analysis v. Design:</mark>

Difficult to draw a boundary

Traditional informal distinction:
- Analysis models the real-world system 
- Design models the software

Object-oriented methods use the same notation for both activities. This encourages '<mark style="background:#69E7E4;">seamless development</mark>' and iteration

### <mark style="background:#69E7E4;">Object Design:</mark>

We need to define attributes and operations for each class in the model

Start from domain model, but:
- Structure of real-world application is not always the optimal structure for a software system
- Domain model does not show operations

<mark style="background:#69E7E4;">Realisation</mark> identifies operations and confirms that design supports functionality

### <mark style="background:#69E7E4;">Object Responsibilities:</mark>

Each class in a system should have well-defined <mark style="background:#69E7E4;">responsibilities</mark>
- To manage a subset of the data in the system
- To manage some of the processing

The responsibilities of a class should be <mark style="background:#69E7E4;">cohesive</mark>
- They should <mark style="background:#69E7E4;">"belong together"</mark>
- They should form a sensible whole

<mark style="background:#69E7E4;">Software Architecture:</mark>

The UP analysis workflow includes the production of an <mark style="background:#69E7E4;">architectural description</mark>, the <mark style="background:#69E7E4;">SAD</mark>

This defines:
- The top-level structure of subsystems
- The role and interaction of these subsystems

Typical architectures are codified in <mark style="background:#69E7E4;">patterns</mark>, e.g. <mark style="background:#69E7E4;">layered architectures</mark>

### <mark style="background:#69E7E4;">A Layered Architecture:</mark>

Subsystems are shown as UML <mark style="background:#69E7E4;">packages</mark> linked by <mark style="background:#69E7E4;">dependencies</mark>

A dependency without a stereotype means <mark style="background:#69E7E4;">uses</mark>

![](https://i.imgur.com/xNDGLTG.png)


### <mark style="background:#69E7E4;">Separation of Concerns:</mark>

Layers aim to insulate a system from the effects of change

For example, user interfaces often change:
- But the application does not use the presentation layer
- So changes to system should be restricted to presentation layer classes

Similarly, details of persistent data storage are separated from application logic

### <mark style="background:#69E7E4;">Analysis Class Stereotypes:</mark>

Within this architecture objects can have various typical roles:
- <mark style="background:#69E7E4;">Boundary</mark> objects interact with outside actors
- <mark style="background:#69E7E4;">Control</mark> objects manage use case behaviour
- <mark style="background:#69E7E4;">Entity</mark> objects maintain data

These are represented explicitly in UML by using analysis class stereotypes

### <mark style="background:#69E7E4;">Class Stereotype Notation:</mark>

Stereotypes can be text or a graphic icon

The icon can replace the normal class box

![](https://i.imgur.com/HapljgP.png)


### <mark style="background:#69E7E4;">Use-Case Realisation:</mark>

Begin with functionality in application layer

<mark style="background:#69E7E4;">'Display bookings'</mark>: simple dialogue
- The user provides the required date
- The system response is to update the display

<mark style="background: #69E7E4;">Initial realisation consists of:</mark>
- Instance of the <mark style="background:#69E7E4;">"Staff"</mark> actor
- An object representing the system
- Message(s) passed between them

<mark style="background:#69E7E4;">System Messages</mark> - from outside the software to the software, i.e. from actor to software system. Could be clicking on an Ok button or entering a number. Documented in use-case descriptions

<mark style="background:#69E7E4;">Internal Messages</mark> - from object to object

The <mark style="background:#69E7E4;">Unified Process</mark> (<mark style="background:#69E7E4;">UP</mark>) advocates the use of a boundary class between the actor and application classes. It receives system messages

However, analysis modelling is chiefly concerned with use-case realisation within the application layer

A boundary class refers to the presentation layer so we can ignore it

In general, there are several system messages in a use-case and it is important that they are handled in the correct order and that appropriate objects respond to them

This is the role of a control object

### <mark style="background:#69E7E4;">System Messages:</mark>

System messages are sent by an actor

Represent system by a <mark style="background:#69E7E4;">controller</mark>, initially analysing use case behaviour, not I/O

![](https://i.imgur.com/S1yR7YW.png)


### <mark style="background:#69E7E4;">Sequence Diagrams:</mark>

Time passes from top to bottom

Instances of classes and actors at top
- Only show those participating in this interaction
- Each instance has a <mark style="background: #69E7E4;">lifeline</mark>

Messages shown as arrows between lifelines
- Labelled with operation name and paramters
- Return messages (dashed) show return of control
- <mark style="background: #69E7E4;">Activations</mark> show when receiver has control

### <mark style="background:#69E7E4;">Accessing Bookings:</mark>

How does the system retrieve the bookings to display?

Which object should have the responsibility to keep track track of all bookings?
- If this was an additional responsibility of the BookingSystem control object it would lose cohesion
- Better to assign responsibility of keeping track of the booking entities to another object
- So define a new "Restaurant" object with the responsibility to manage booking data

### <mark style="background:#69E7E4;">Retrieving Bookings:</mark>

Add a message to get relevant bookings

'updateDisplay' is an internal message. In actuality, it will be sent to presentation layer object

![](https://i.imgur.com/tDxA0a8.png)


Dates of individual bookings will need to be checked by the Restaurant object

![](https://i.imgur.com/UIlkXnY.png)


### <mark style="background:#69E7E4;">Refining the Domain Model:</mark>


New <mark style="background:#69E7E4;">'Restaurant'</mark> and <mark style="background:#69E7E4;">'BookingSystem'</mark> classes, with an association between them

An association from <mark style="background:#69E7E4;">'Restaurant'</mark> to <mark style="background:#69E7E4;">'Booking'</mark>
- <mark style="background:#69E7E4;">'Restaurant'</mark> maintains links to all bookings
- Messages sent from restaurant to bookings

An association from <mark style="background:#69E7E4;">'BookingSystem'</mark> to <mark style="background:#69E7E4;">'Booking'</mark>
- <mark style="background:#69E7E4;">'BookingSystem'</mark> maintains links to currently displayed bookings

### <mark style="background:#69E7E4;">Updated Class Diagram:</mark>

Operations are derived from messages sent to the instances of a class

![](https://i.imgur.com/SrNCf0w.png)


### <mark style="background:#69E7E4;">Recording New Bookings:</mark>

Give 'Restaurant' responsibility for creation, don't model details of user input or data yet

![](https://i.imgur.com/wuWhDEy.png)


### <mark style="background:#69E7E4;">Creating a New Booking:</mark>

Bookings must be linked to table and customer objects. Responsibility of 'Restaurant' to retrieve these, given identifying data in booking details

New objects shown at point of creation:
- Lifeline starts from that point
- Objects created by a message arriving at the instance (a <mark style="background: #69E7E4;">constructor</mark>)

![](https://i.imgur.com/LWQ5wG5.png)



### <mark style="background:#69E7E4;">Cancelling a Booking:</mark>

A three-stage process:
- Select on screen the booking to be cancelled
- Confirm cancellation with user
- Delete the corresponding booking object

Object deletion represented by a message with a 'destroy' stereotype, lifeline terminates with an 'X'

<mark style="background:#69E7E4;">Role</mark> <mark style="background:#69E7E4;">names</mark> are used to distinguish selected object from others displayed

- ![](https://i.imgur.com/OdteGDH.png)


### <mark style="background:#69E7E4;">Refining the Domain Model (2)</mark>

'BookingSystem' has the responsibility to remember which booking is selected

Add an association to record this

![](https://i.imgur.com/PW6vJdl.png)


### <mark style="background:#69E7E4;">Recording Arrival:</mark>

- Selected booking must be a reservation

![](https://i.imgur.com/gmm9LZj.png)


### <mark style="background:#69E7E4;">Class Interface Design:</mark>

Should 'setArrivalTime' be defined in Booking or Reservation class?
- On one hand, it doesn't apply to walk-ins
- But we want to preserve a common interface to all bookings if possible

Define operation in 'Booking' class:
- Default implementation does nothing
- Override in 'Reservation' class

### <mark style="background:#69E7E4;">Refined Class Hierarchy:</mark>

   ![](https://i.imgur.com/waigHvk.png)


### <mark style="background:#69E7E4;">Summary:</mark>

Analysis has led to:
- A set of use-case realisations
- A refined class diagram
 
We can see how the class design is going to support the functionality of the use cases

This gives confidence that the overall design will work

### <mark style="background:#69E7E4;">Complete Analysis Class Model:</mark>

   ![](https://i.imgur.com/ediQJUr.png)

# <mark style="background: #69E7E4;">04. Practical OO Design with UML</mark>

 

### <mark style="background: #69E7E4;">Specifying Behaviours:</mark>

Interaction diagrams:
- show how object behave in particular interactions
- do not specify all the possible behaviours of objects

Different notation is needed to summarise the overall behaviour of objects UML defines <mark style="background: #69E7E4;">statecharts</mark> for this purpose

### <mark style="background: #69E7E4;">State-dependent Behaviour:</mark>

Objects respond differently to the same stimulus at different times

This is modelled by defining a set of <mark style="background: #69E7E4;">states</mark>:
- an object can be in one state at any time
- the state it is in determines how it responds to <mark style="background: #69E7E4;">events</mark> detected or messages received
- in particular, an event can cause the object to move from one state to another (a <mark style="background: #69E7E4;">transition</mark>)

### <mark style="background: #69E7E4;">States, Events and Transitions:</mark>

A simple state chart for a CD player:
![](https://i.imgur.com/pUylBrY.png)

### <mark style="background: #69E7E4;">Statechart Semantics:</mark>

A <mark style="background: #69E7E4;">statechart</mark> defines the behaviour of instances of a given class

An object is in one <mark style="background: #69E7E4;">active state</mark> at a time

<mark style="background: #69E7E4;">Events</mark> may be received at any time

An event can <mark style="background: #69E7E4;">trigger</mark> a transition: a transition from the active state will <mark style="background: #69E7E4;">fire</mark> if it is labelled with the event just received    

The transition leads to the next active state

### <mark style="background: #69E7E4;">Initial and Final States:</mark>

Model the creation and destruction of objects.

![](https://i.imgur.com/hLW8R0A.png)

### <mark style="background: #69E7E4;">Non-determinism:</mark>

Sometimes there are two transitions with the same event label leaving a state

![](https://i.imgur.com/EB2SRvV.png)

Some systems are non-deterministic but usually the non-determinism can be removed by adding more information

### <mark style="background: #69E7E4;">Guard Conditions:</mark>

<mark style="background: #69E7E4;">Conditions</mark> added to events indicate when a transition can fire

![](https://i.imgur.com/zg79Jy6.png)

### <mark style="background: #69E7E4;">Actions:</mark>

Actions are performed when a transition fires

![](https://i.imgur.com/CYyzfjI.png)

### <mark style="background: #69E7E4;">Entry and Exit Actions:</mark>

Entry and exit actions are properties of states

They are performed whenever an object arrives at or leaves the state, respectively.

![](https://i.imgur.com/4wp69Vk.png)

### <mark style="background: #69E7E4;">Activities:</mark>

Activities are also properties of states
- they are performed while the object is in a state
- unlike actions, they can be interrupted by new events

![](https://i.imgur.com/gWcNOmz.png)

### <mark style="background: #69E7E4;">Completion Transitions:</mark>

If an activity completes uninterrupted it can trigger a <mark style="background: #69E7E4;">completion transaction</mark>: these are transitions without event labels

![](https://i.imgur.com/7y1dDwy.png)

### <mark style="background: #69E7E4;">Internal Transitions:</mark>

Internal transitions do not change state and so do not execute entry and exit actions

![](https://i.imgur.com/kiTl4CH.png)

### <mark style="background: #69E7E4;">Composite States:</mark>

Composite states group together states, this can simplify a statechart by grouping together states with similar behaviour

An object still has one ‘bottom-level’ active state, but may be in a composite state as well.

![](https://i.imgur.com/VQO5Fz7.png)

### <mark style="background: #69E7E4;">Properties of Composite States:</mark>

<mark style="background: #69E7E4;">Transitions:</mark> 
- <mark style="background: #69E7E4;">from</mark> a composite state apply to all substates
- <mark style="background: #69E7E4;">to</mark> a composite state go to the state indicated by a nested initial state
- can cross composite state boundaries

Composite states can have activities and  entry and exit actions

A final state in a composite triggers a completion transition from the composite

### <mark style="background: #69E7E4;">A complex composite state:</mark>

![](https://i.imgur.com/gRdbSC0.png)

### <mark style="background: #69E7E4;">History States:</mark>

Often an object needs to ‘return to the previous state’

This can be done by defining conditions (such as ‘if the last state was Playing’)

Composite states can have a <mark style="background: #69E7E4;">history</mark> state
- this ‘remembers’ the last active substate    
- a transition to a history state makes that substate active again

### <mark style="background: #69E7E4;">Use of a History State:</mark>

![](https://i.imgur.com/pLVOIxr.png)

### <mark style="background: #69E7E4;">Complete CD Player Statechart:</mark>

![](https://i.imgur.com/N9vP7mp.png)

### <mark style="background: #69E7E4;">Creating a Statechart:</mark>

It can be hard to identify all necessary states    

Statecharts can be developed incrementally    
- consider individual sequences of events received by an object
- these might be specified on interaction diagrams
- start with a statechart for one interaction
- add states as required by additional interactions

### <mark style="background: #69E7E4;">Ticket Machine:</mark>

Consider a ticket machine with two events    
- select a ticket type
- enter a coin

Basic interaction is to select a ticket and then enter coins (model this as a ‘linear’ statechart)

![](https://i.imgur.com/O0epmBq.png)

### <mark style="background: #69E7E4;">Refining the Statechart:</mark>

This can be improved by adding ‘loops’    
- the number of coins entered will vary: entry will continue until the ticket is paid for
- the whole transaction can be repeated

![](https://i.imgur.com/xrzObU3.png)

### <mark style="background: #69E7E4;">Adding Another Interaction:</mark>

The user could enter a coin before selecting a ticket     
A ‘coin’ transition from the ‘Idle’ state is needed to handle this event    
- this transition can’t go to the ‘Paying for Ticket’ state as the ticket is not yet selected
- so a new state ‘Inserting Coins’ is required

The statechart is thus built up step-by-step.

### <mark style="background: #69E7E4;">Adding a Second Interaction:</mark>

If all coins are entered before ticket selected:
![](https://i.imgur.com/pPs7PGE.png)


### <mark style="background: #69E7E4;">Integrating the Interactions:</mark>

In fact, events can occur in any sequence:

![](https://i.imgur.com/dUpwGNi.png)

### <mark style="background: #69E7E4;">Time Events:</mark>

Suppose the ticket machine times out after 30 seconds 
- we need to fire a transition that is not triggered by a user-generated event
- UML define <mark style="background: #69E7E4;">time</mark> events to handle these cases

![](https://i.imgur.com/qwZJcdH.png)

### <mark style="background: #69E7E4;">Activity States:</mark>

<mark style="background: #69E7E4;">Activity states</mark> defines periods of time when the object is carrying out internal processing
- unlike normal activities, these cannot be interrupted by external events
- only <mark style="background: #69E7E4;">completion</mark> transitions leading from them
- useful for simplifying the structure of complex statecharts

### <mark style="background: #69E7E4;">Returning Change:</mark>

Use an activity state to calculate change
![](https://i.imgur.com/P0AGcy3.png)

### <mark style="background: #69E7E4;">Ticket Machine Statechart:</mark>

![](https://i.imgur.com/XVMbEF3.png)

# <mark style="background: #69E7E4;">05. Agile Process Models</mark>

 

### <mark style="background:#69E7E4;">Agile Methodologies:</mark>

Traditional IS development methodologies "are treated primarily as a necessary fiction to represent an image of control or to provide a symbolic status"

Lightweight alternative to traditional heavyweight processes

Began with introduction of extreme programming (XP) by Beck in 1999.

Agile manifesto in 2001

A number of other methods have been invented or rediscovered since

However, no clear agreement on how to distinguish Agile from Traditional Methodologies

### <mark style="background:#69E7E4;">Agile values:</mark>

  Individuals and interactions over tools and processes

Working software over comprehensive documentation - continuously turn out working tested software

Customer collaboration over contract negotiation

Responding to change rather than following a plan - adaptive rather than prescriptive

### <mark style="background:#69E7E4;">Agile characteristics & principles:</mark>

Satisfy the customer through early and continuous delivery of valuable software

Incremental and timebound with short iteration cycles from 1 to 6 weeks

Development group consists of both software developers and customer representatives. Regular feedback is given to developers. Authorised to consider adjustments during developments.

Working software is the primary measure of progress

What is new is the recognition of people as the primary drivers of project success along with intense focus and manoeuvrability

Fully automated regression testing testing

Experienced developers - speeds up project by a factor anywhere from 2 to 10 times

Minimal process overheads, remove unnecessary process activities

Modelling tools are not as useful as generally thought

Continuous attention to technical excellence, e.g. refactoring in XP

At regular intervals, the team reflects on how to become more effective, then tunes and adjusts its behaviour accordingly

### <mark style="background:#69E7E4;">Agile methodologies:</mark>

- Extreme Programming (XP)
- Scrum
- Crystal
- Feature driven development
- UP?

### <mark style="background:#69E7E4;">XP Lifecycle:</mark>

- ![](https://i.imgur.com/cAKhCg9.png)


### <mark style="background:#69E7E4;">Exploration Phase:</mark>

Customers write story cards for first release

Each story card describes features of system (like a brief use-case)

Project team familiarise themselves with tools, technology and practices they use in the project.

Try out tools and explore possibilities for architecture via prototyping

Phase can take from a few weeks to a few months

Set priorities from a few weeks to a few months

### <mark style="background:#69E7E4;">Planning phase:</mark>

Set priority for stories

Agree contents of first small release

Estimate effort for each story and agree schedule

First release normally not more than two months

Planning phase itself takes a couple of days

### <mark style="background:#69E7E4;">Iterations to Release Phase:</mark>

Several iterations from 1 to 4 weeks

First iteration creates a system with architecture for the whole system

Select story that will enforce building of structure for whole system

Customer selects stories for each iteration

Functional tests created by customer run at the end of each iteration

### <mark style="background:#69E7E4;">Productioning Phase:</mark>

Requires extra testing and performance checking before being released to a customer

New changes may still be found

Shorter iterations

### <mark style="background:#69E7E4;">Maintenance and Death Phase:</mark>

Keep system in production while producing new increments

Requires effort for customer support tasks

Development speeds may slow

Maybe incorporate new people into team

Death phase - no more stories to be implemented, or if system not delivering desired outcomes or is proving too expensive for development

### <mark style="background:#69E7E4;">XP Roles:</mark>

<mark style="background:#69E7E4;">Programmer</mark>

<mark style="background:#69E7E4;">Customer</mark> - writes stories and functional tests

<mark style="background:#69E7E4;">Tester</mark> - gives feedback on schedule to team

<mark style="background:#69E7E4;">Coach</mark> - has sound understanding of XP

<mark style="background:#69E7E4;">Consultant</mark> - specific technical knowledge

<mark style="background:#69E7E4;">Manager</mark>

### <mark style="background:#69E7E4;">XP Practices:</mark>

Planning game

Small short releases

<mark style="background:#69E7E4;">Simple design</mark> - simplest possible design that is implementable at the moment

<mark style="background: #69E7E4;">Testing</mark> - development is test driven. Unit tests are implemented before code and run continuously. Customers write functional tests

Refactoring

Pair programming

<mark style="background:#69E7E4;">Collective ownership</mark> - anyone can change any part any time.

<mark style="background: #69E7E4;">Continuous integration</mark> - new piece of code integrated into code-base as soon as it is ready. System integrated and built many times daily. All tests run and have to be passed for change to be accepted.

40 hour week

On site customer

Open workspace

### <mark style="background:#69E7E4;">XP - Scope of Use:</mark>

Small to medium sized teams, 3 to 20 project members

Communication between members at all times, even scattering across two floors is not acceptable

Any resistance by team members, management or customers may fail the process

Growing research

### <mark style="background:#69E7E4;">Scrum:</mark>

Developed for managing the Systems Development process.

No specific software development technique, can be adopted to manage an organisation's own engineering practices

Focuses on flexibility of team members in producing software in a constantly changing environment

Frequent management activities to identify and rectify any impediments in the development process

Suitable for small teams of less than 10.

Development relies on several Environmental and technical variables which are likely to change
- Requirements
- Time frame
- Resources
- Technology
- Development Methods

### <mark style="background:#69E7E4;">Scrum Lifecycle:</mark>

![](https://i.imgur.com/Zef2rMa.png)


### <mark style="background:#69E7E4;">Scrum - 3 phases:</mark>

Pregame phase, which consists of 2 sub-phases
- Planning
- Architecture and High-level design

Development or Game Phase
Postgame phase

### <mark style="background:#69E7E4;">Pregame planning sub-phase:</mark>

<mark style="background:#69E7E4;">Product Backlog list:</mark>
- All requirements that are currently know
- Prioritised
- Development effort estimated

Includes definition of team, tools and other resources

Risk Assessment

Training needs

### <mark style="background:#69E7E4;">Pre-game architecture sub-phase:</mark>

High level design of system including architecture planned based on current Product Backlog

For enhancement to an existing system, changes needed for implementing backlog are identified along with any problems they may cause.

Design review meetings are held to go over proposals. Decisions are made on the basis of this review

### <mark style="background:#69E7E4;">Development or Game Phase:</mark>

Agile part of Scrum, unpredictable expected.

System developed in Sprints
- Iterative cycles where functionality is developed or enhanced to produce new increments.
- Included traditional development activities of analysis, design, implementation, delivery
- A Sprint is planned to last from 1 week to 1 month
- Could be 3 to 8 sprints in a system development process before ready for distribution.

Environment and technical variables are observed and controlled during sprints, not just at beginning.

### <mark style="background:#69E7E4;">Postgame Phase:</mark>

- Entered when agreement reached that
- environmental variables such as requirements are completed
- System ready for release
- Integration
- System Testing
- Documentation

### <mark style="background:#69E7E4;">Scrum Roles & Responsibilities:</mark>

<mark style="background:#69E7E4;">Six roles:</mark>
- Scrum Master
- Product Owner
- Scrum Team
- Customer
- User
- Management

<mark style="background:#69E7E4;">Scrum Master:</mark>
- Responsible for ensuring that project is run according to practices, values and rules of Scrum.
- Interacts with team, customer and management.
- Responds to impediments

<mark style="background:#69E7E4;">Product Owner:</mark>
- Responsible for managing and controlling backlog list
- Selected by Scrum Master, Customer and Management
- Makes final decisions on backlog, decides on features to be developed, estimates development effort.

<mark style="background:#69E7E4;">Scrum Team:</mark>
- Self organising in order to achieve goals

<mark style="background:#69E7E4;">Customer:</mark>
- participates in creating product backlog

<mark style="background:#69E7E4;">Management:</mark>
- In charge of final decision making
- Also involved in selecting Product Owner
- Gauging progress with Scrum Master

# <mark style="background: #69E7E4;">06. Use Quick Tour</mark>

 

# <mark style="background:#69E7E4;">USE Quick Tour</mark>
This quick tour will demonstrate the main features of USE.

### <mark style="background:#69E7E4;">1. Example Model</mark>

Consider the following UML class diagram for a simple model describing employees, departments, projects, and their relationships to each other.

![](https://www.db.informatik.uni-bremen.de/projects/USE-2.3.1/gen-img/cls-EDP.png)

We extend the model by the following four constraints which place further restrictions on systems conforming to the model. The constraints are first given in natural language and will later be expressed more formally in OCL (Object Constraint Language).

<mark style="background:#69E7E4;">Constraints:</mark>
- The number of employees working in a department must be greater or equal to the number of projects controlled by the department.
- Employees get a higher salary when they work on more projects.
- The budget of a project must not exceed the budget of the controlling department.
- Employees working on a project must also work in the controlling department.
    
The goal of applying the USE tool is to interactively validate the above model and the constraints. Objects and links can be created which constitute a system state reflecting a snapshot of a running system. In every system state, the constraints are automatically checked for validity.

### <mark style="background:#69E7E4;">2. USE Specifications</mark>

The USE tool expects as input a textual description of a model and its constraints. The above class diagram must therefore be first translated into a USE specification (a possible extension to USE would be the import of an XMI file created by a CASE tool like [Argo UML](http://argouml.tigris.org/) or Rational Rose.). The first part of the specification shown below describes the structural information of the class diagram.

```
model Company

-- classes

class Employee
attributes
  name : String
  salary : Integer
end

class Department
attributes
  name : String
  location : String
  budget : Integer
end

class Project 
attributes
  name : String
  budget : Integer
end

-- associations

association WorksIn between
  Employee[*]
  Department[1..*]
end

association WorksOn between
  Employee[*]
  Project[*]
end

association Controls between
  Department[1]
  Project[*]
end
``` 

    
- In the second part of the specification, we define the constraints in OCL. Each constraint is defined as an invariant in context of a class.
    
```
-- OCL constraints

constraints

context Department 
    -- the number of employees working in a department must
    -- be greater or equal to the number of projects 
    -- controlled by the department
  inv MoreEmployeesThanProjects:
    self.employee->size >= self.project->size 

context Employee 
    -- employees get a higher salary when they work on
    -- more projects
  inv MoreProjectsHigherSalary:
    Employee.allInstances->forAll(e1, e2 | 
      e1.project->size > e2.project->size 
        implies e1.salary > e2.salary)

context Project
    -- the budget of a project must not exceed the 
    -- budget of the controlling department
  inv BudgetWithinDepartmentBudget:
    self.budget <= self.department.budget

    -- employees working on a project must also work in the
    -- controlling department
  inv EmployeesInControllingDepartment:
    self.department.employee->includesAll(self.employee)
```
    
The complete specification is also available in the file [Demo.use](https://www.db.informatik.uni-bremen.de/projects/USE-2.3.1/Demo.use) in the example directory of the distribution.

### <mark style="background:#69E7E4;">3. Running USE</mark>

The following command can be used to invoke USE on the example specification (assuming the current working directory is the top-level directory of the distribution and the bin directory is added to your PATH environment variable).

 ``use examples/Demo.use``

This command will compile and check the file Demo.use. There are currently two kinds of user interfaces which can be used simultaneously. The first one is a command line interface where you enter commands at a prompt. The output should be similar to the following.

```
loading properties from: /home/mr/use/etc/use.properties
use version 2.3.1, Copyright (C) 1999,2000 Mark Richters
compiling specification... 
Model Company (3 classes, 3 associations, 4 invariants, 0 operations) 
Enter 'help' for a list of available commands. 
use>
```

At this point you can enter commands at the prompt (try 'help' for a list of available commands). For example, you can enter OCL expressions by starting the input with a question mark. The expression will be evaluated and its result will be shown, e.g.:

``use> **? Set{1,2,3}->select(e | e > 1) **-> Set{2,3} : Set(Integer)``


The command line interface is useful for experienced users and for automated validation procedures since commands can be read from a script file. The graphical user interface is easier to learn and provides different ways of visualizing a system state. By default both interfaces are launched (unless you specify the switch`` -nogui`` at startup time).

### <mark style="background:#69E7E4;">4. The Graphical User Interface</mark>

Let's get back to the example. The window that appears after starting USE can be seen in the following screen shot (click on the picture to get an enlarged version).

![](https://i.imgur.com/WsDs1Bx.png)

On the left is a tree view showing the contents (classes, associations, invariants, and pre- and postconditions) of the model. The next picture shows the expanded tree with all model elements. One of the invariants is selected and its definition is shown in the panel below the tree.

![](https://i.imgur.com/FFdlOnb.png)

The large area on the right is a workspace where you can open views visualizing different aspects of a system. Views can be created any time by choosing an entry from the view menu or directly by a toolbar button. There is no limit on active views. The next screen shot displays the main window after the creation of four views.

![](https://i.imgur.com/vBAUDhJ.png)

The two upper views list the names of classes and associations defined in the model and shows the number of objects and links in the current system state. The initial system state is empty, i.e., there are no objects and links yet. The view at the lower left displays a list of OCL invariants and their results. As you can see, all invariants are true in the empty system state. Finally, the lower right view will show an object diagram once we have created objects and links.

### <mark style="background:#69E7E4;">5. Creating Objects and Setting Attributes</mark>

Objects can be created by selecting a class and specifying a name for the object. The menu command ``State|Create object`` opens a dialog where this information can be entered.

![](https://i.imgur.com/YkoTH2d.png)

Alternatively, the following command can be used at the prompt to achieve the same effect.

``use> !create cs:Department

And, even simpler, an object can be created via drag & drop. Just select a class in the model browser and drag it to the object diagram.

Note the change in the system state views. The upper right view indicates that there is now one department object, and the object diagram shows this object graphically.

![](https://i.imgur.com/GOWjAFe.png)


A context menu available on a right mouse click in the object diagram provides several display options. For example, the automatic layout can be turned off, the layout of the diagram can be saved and restored from a file, etc. In the previous picture we have turned on the display of attribute values. You can see that the attribute values of the department object are all undefined. For changing attribute values, we can use the set command:

```
use> !set cs.name := 'Computer Science' 
use> !set cs.location := 'Bremen' 
use> !set cs.budget := 10000
```

Attributes can also be changed with an _object properties view_. If you choose ``View|Create|Object Properties`` from the View menu and select the ``cs`` object, you get the following view where you can inspect and change attributes of the selected object:

![](https://i.imgur.com/oiT00Ta.png)


We continue by adding two employee objects and setting their attributes (Again, we use the command line interface here, but the same can be achieved by using the previously discussed steps in the graphical user interface).
```
use> !create john : Employee 
use> !set john.name := 'John' 
use> !set john.salary := 4000 
use> !create frank : Employee 
use> !set frank.name := 'Frank' 
use> !set frank.salary := 4500
```

Now we have three objects, a department and two employees, but still no connections between them. The layout in the object diagram is continuously refined and updated. This can be turned off by deselecting the option Auto-Layout in the context menu of the object diagram.

The previous commands resulted in an invalid system state. This is discussed in detail in the next section.

![](https://i.imgur.com/9scgM88.png)


### <mark style="background:#69E7E4;">6. Model Inherent Constraints</mark>

The invariant view indicates some problem with the new system state. The message says: _Model inherent constraints violated_. Model inherent constraints are constraints defined implicitly by a UML model (in contrast to explicit OCL constraints). The details about this message are shown in the Log panel at the bottom of the screen (they are also available by issuing a check command at the prompt):

 
```
use> check
Multiplicity constraint violation in association WorksIn´:
  Object frank´ is connected to 0 object(s) of class Department´
  but the multiplicity is specified as 1..*'.
Multiplicity constraint violation in association WorksIn´:
  Object john´ is connected to 0 object(s) of class Department´
  but the multiplicity is specified as 1..*'.
```

The problem here is that we have specified in the model that each employee has to be related to at least one department object (see the class diagram above). In our current state, no employee has a link to a department. In order to fix this, we insert the missing links into the WorksIn association:

```
use> !insert (john,cs) into WorksIn 
use> !insert (frank,cs) into WorksIn
```

Links can also be inserted by selecting the objects to be connected in the object diagram and choosing the ``insert`` command from the context menu.

The new state shows the links in the object diagram as red edges between the employee objects and the department object. The invariants are satisfied again.

![](https://i.imgur.com/VtwUhSi.png)


### <mark style="background:#69E7E4;">7. Checking OCL Invariants</mark>

We have seen that class invariants are checked automatically each time a system state changes. This section shows how invariants can be analyzed. We continue the example by adding two projects and linking them to the existing employees and the department:
```
use> !create research : Project
use> !set research.name := 'Research'
use> !set research.budget := 12000
use> 
use> !create teaching : Project
use> !set teaching.name := 'Validating UML'
use> !set teaching.budget := 3000
use> 
use> !insert (cs,research) into Controls
use> !insert (cs,teaching) into Controls
use> 
use> !insert (frank,research) into WorksOn
use> !insert (frank,teaching) into WorksOn
use> !insert (john,research) into WorksOn
```

The resulting state is shown below.

![](https://i.imgur.com/eruG4MX.png)

In this state, three of the four invariants are true but one fails. The failing one has the name BudgetWithinDepartmentBudget. This invariant states that The budget of a project must not exceed the budget of the controlling department. Obviously, one of the two projects in our example must have a budget higher than the budget of the department.

The value false finally resulting from an evaluation of an invariant is not very helpful in finding the reason for an illegal system state. An _evaluation browser_ provides a more detailed view of an expression by showing the results of all sub-expressions. Double-clicking on an invariant will open an evaluation browser:

![](https://i.imgur.com/Qq65WWp.png)


The root node in the evaluation browser shows the complete expression and its result (which is false for the chosen invariant). For each component of an expression there are child nodes displaying the sub-expressions and their results. You can see that the argument expression of the forAll quantifier is false, thus making the whole expression result false. In this sub-expression, the variable self is bound to the object research. The evaluation browser has helped to find out that it is the budget attribute value of this object which causes the invariant to fail.

### <mark style="background:#69E7E4;">8. Evaluating OCL Expressions</mark>

The OCL parser and interpreter of USE allows the evaluation of arbitrary OCL expressions. The menu item ``State|Evaluate OCL`` expression opens a dialog where expressions can be entered and evaluated.

![](https://i.imgur.com/Z8gBQlX.png)

The following example shows a complex expression navigating from a department over projects to employees. The expression finds all projects of the computer science department in which an employee called john is involved.

![](https://i.imgur.com/uBhUGDn.png)

# <mark style="background: #69E7E4;">07. Design by Contract</mark>

 

# <mark style="background: #69E7E4;">Design by Contract - beyond Class Modelling</mark>


### <mark style="background: #69E7E4;">Introduction</mark>

<mark style="background: #69E7E4;">Design by Contract (DbC</mark>) or Programming by Contract is an approach to designing software.

It says that designers should define precise and verifiable interface specifications for software components, with the use of preconditions, postconditions and invariants. These specifications are referred to as "contracts"; in the same way as a business contract entails certain obligations and conditions.

- developed by Bertrand Meyer, “Bubbles (aka UML boxes) don’t crash”, and forms a central feature of Eiffel
- uses <mark style="background: #69E7E4;">assertions</mark> – assertion is a Boolean statement that should never be false. If so, it indicates a bug
- assertions usually only checked during debugging/testing

- <mark style="background: #69E7E4;">Three kinds of assertions:</mark>
	- post-conditions
	- pre-conditions
	- invariants
	
- pre-conditions and post- conditions are associated with operations
	
### <mark style="background: #69E7E4;">Pre-condition:</mark>

- expresses something about the state of a program that should be true before an operation is executed
- e.g. a pre-condition for an integer-square-root operation might be 
- ``input >= 0``
- indicates it is an error to invoke square-root on a negative number
- e.g. ``pop()`` should net be called on an empty stack, precondition is
- ``s.isEmpty() == false``
- makes explicit that the calling routine is responsible for ensuring that something is true before operation is invoked
- lack of one may lead to too little or too much checking (duplicate checking code and thus more complicated program)
- 
### <mark style="background: #69E7E4;">Post Condition:</mark>

- a statement of what things should be like after the execution of an operation
- e.g. <mark style="background: #69E7E4;">integer-square-root</mark> operation
- ``result * result <= input < (result+1)*(result+1)``
- expresses <mark style="background: #69E7E4;">what</mark> an operation does rather than <mark style="background: #69E7E4;">how</mark> it does it
- separates implementation from interface
- leads to a stronger definition of an <mark style="background: #69E7E4;">exception</mark>. Exception occurs when an operation is invoked with its pre-condition satisfied and is unable to return with its post-condition true

### <mark style="background: #69E7E4;">Benefits - Obligations</mark>

![](https://i.imgur.com/3dC35Fg.png)


### <mark style="background: #69E7E4;">Spec# Example:</mark>

http://www.rise4fun.com/SpecSharp

The following shows a C# implementation of integer square-root() where the precondition (requires) and postcondition (ensures) are described in Spec#. Spec# supports DbC for C#. They form a contract for the method. It can be proved that the method code satisfies the contract.

```C#
class Fig1 {
	int ISqrt(int x)
		requires 0 <= x;
		ensures result*result <= x && x < (result+1)*(result+1);
	{
		int r = 0;
		while ((r+1)*(r+1) <= x)
			invariant r*r <= x;
		{
			r++;
		}
		
		return r;
	}
}
```

### <mark style="background: #69E7E4;">Invariant:</mark>

- an assertion about a class or a method
- invariant is always true for class instances – meaning whenever object is available for an operation to be invoked on it
- may be temporarily false during execution of method
- e.g. Account class ``balance == sum of transaction amounts``
- e.g. in the above Spec# example, ``r*r <= x`` is an invariant of the while loop
- invariant is added to pre-conditions and post-conditions of public methods

### <mark style="background: #69E7E4;">Subclassing/Polymorphism:</mark>

- Assertions useful with polymorphism, assertions can help keep subclass operations consistent with those of superclass invariants and post-conditions must be true for all subclasses, subclass can strengthen these, i.e. make them more restrictive

- Not allowed to strengthen pre-conditions – because of substitutability, can only weaken a pre-condition,

- If a subclass strengthened a pre-condition, then a superclass operation could fail when applied to instance of subclass

- Pre-conditions: best pay-off for least overhead

- One language to support assertions is Eiffel

### <mark style="background: #69E7E4;">DbC and OCL:</mark>

The following material is largely drawn from the text: Model Driven Architecture – Applying MDA to Enterprise Computing by David S. Frankel.

The following class diagram is to be used with the DbC constraints described in OCL on the following page. Note that DbC does not have to use OCL (object constraint language). OCL is now officially part of UML 2.0.

![](https://i.imgur.com/mn79eeA.png)

![](https://i.imgur.com/URyXm4f.png)

![](https://i.imgur.com/OsXTT6t.png)

<mark style="background: #69E7E4;">DbC constraints have two basic purposes:</mark>
- highlighting unacceptable corner case
- expressing key semantics of class or operation to which they apply

E.g. ``ReceivableAccount`` invariant indicates that an invoice cannot be both processed and
unprocessed.

Post-condition for ``EndOfMonthUpdate()`` says in platform-independent fashion that current balances need to be rolled over to 30 day balances. Reflects a business rule.

Similarly, ``EndOfMonthUpdate()`` pre-condition that there should be no unprocessed invoices
reflects another business rule.

Constraints nail down properties of classes without predetermining platform specific techniques for implementing them.

Contracts are useful to clients and generators. OCL constraints flesh out the model and connect the dots for generators and programmers and help discover design flaws.

The more precisely a classes properties are specified, the easier it is to reuse the class. OO and component based development promise reuse as major advantage. But developers find class or component reuse difficult without access to source code because the usage contract is not well specified.

Interoperability between components from different companies also an issue even when components support standardised interfaces, messages and protocols unless there is a good understanding of the contract that the interface must honour when implemented. 

Important to Java Community process, OMG, and B2Bi initiatives.

Interoperability is based on shared understanding among interoperating objects.
- Syntactic interoperability – e.g. CORBA’s IDL & IIOP allow shared understanding of operation signature. Allows values to pass thru all transport layers transparently.
- Semantic interoperability based on objects’ ability to coordinate their functioning based on a shared understanding of the semantics.
- Formal DbC contracts improve semantic interoperability. Hence have an important contribution to make to B2Bi.

### <mark style="background: #69E7E4;">Precision versus Detail:</mark>


DbC constraint writing in OCL is a form of coding. It is more abstract than 3GL programming as it omits many implementation details that are necessary in a 3GL. But it is still no less precise than 3GL.

Example of an electric motor to illustrate precision versus detail. Spec can very precise while giving no detail as to internals of motor. Abstraction is suppression of irrelevant detail, not vagueness.

Can infer exceptions for operations from DbC constraints. Pre-condition maps directly to an exception to be thrown when the operation is invoked and the precondition is not satisfied.

A lot of tool support now available for checking constraints at runtime, e.g. with Spec#. Generate code for checking constraints. Can specify when in time they are to be checked.

### <mark style="background: #69E7E4;">DbC and QA:</mark>

DbC can provide a framework for quality assurance (QA). Pre-conditions, post-conditions and
invariants represent much of what QA engineer must validate. DbC constraints can be used by code generators to produce test harnesses or for program verification as in Boogie tool with Spec#.

Even when not used automatically, DbC constraints act as precise guides to QA engineers regarding what they must test. Also useful for code reviews or walk throughs.

There are other non-functional factors such as scalability and performance, that are not covered by DbC assertions. Can use other UML extension for these.

### <mark style="background: #69E7E4;">Tool Support:</mark>

Many tools have slots for associating constraints with classes and operations.

MDA tools may include OCL editing facilities for writing OCL assertions, similar to IDEs for 3GLs.

Main barrier to effective use of DbC is software development pressure. Rigorous DbC can be time consuming. However, MDA DbC may be timesaving as generators elaborate each formal constraint into many lines of application and test harness code.

Without MDA, DbC only addresses quality. With MDA, it can help with production costs.

### <mark style="background: #69E7E4;">Comment:</mark>

UML class diagrams act as constraints on instances of those classes. OCL describes other constraints that class diagram cannot show.

### <mark style="background: #69E7E4;">Behavioural Modelling:</mark>

Class models with DbC do not describe control flow and state changes inside code. Do not detail how objects interact. They are static structure models rather than behavioural models such as use cases, state machines, activity diagrams and sequence diagrams.

However a DbC based class does describe behaviour when it specifies pre and post-conditions for the class operations. But it strictly confines itself to aspects of behaviour relevant to a client. See example below.

Behavioural modelling is at least as important to MDA as static modelling. Some of the most advanced industrial MDA is based on behavioural modelling. E.g. Shlaer-Mellor systems use state machines to generate embedded code for things like photocopiers and telecom switches.

State machines fall into two categories. One deals with transitions of public class attributes, i.e. attributes visible to clients and thus part of the contract (protocol state machines).

For a DbC class, all the info in such a state machines would also be available in the class model (see following example). Protocol state machine is another representation of info available that a correct DbC-based class model provides. Note, DbC constraints can convey more and be more complex than a state machine.

![](https://i.imgur.com/916szic.png)

![](https://i.imgur.com/8FvtDIu.png)

# <mark style="background: #69E7E4;">08. Design Pattern - Adapter</mark>

 
### <mark style="background: #69E7E4;">Intent:</mark>
Convert the interface of a class into another interface clients expect. Adapter lets
classes work together that couldn't otherwise because of incompatible interfaces. Also
known as Wrapper

### <mark style="background: #69E7E4;">Motivation:</mark>

Sometimes a toolkit class that's designed for reuse isn't reusable only because its interface doesn't match the domain-specific interface an application requires.

Consider for example a drawing editor that lets users draw and arrange graphical elements (lines, polygons, text, etc.) into pictures and diagrams. The drawing editor's key abstraction is the graphical object, which has an editable shape and can draw itself. The interface for graphical objects is defined by an abstract class called Shape.

The editor defines a subclass of Shape for each kind of graphical object: a ``LineShape`` class for lines, a ``PolygonShape`` class for polygons, and so forth.

Classes for elementary geometric shapes like ``LineShape`` and ``PolygonShape`` are rather easy to implement, because their drawing and editing capabilities are inherently limited. But a ````TextShape```` subclass that can display and edit text is considerably more difficult to implement, since even basic text editing involves complicated screen update and buffer management. Meanwhile, an off-the-shelf user interface toolkit might already provide a sophisticated ````TextView```` class for displaying and editing text. Ideally we'd like to reuse ````TextView```` to implement ````TextShape````, but the toolkit wasn't designed with Shape classes in mind. So we can't use ````TextView```` and Shape objects interchangeably.
How can existing and unrelated classes like ````TextView```` work in an application that expects classes with a different and incompatible interface? We could change the ````TextView```` class so that it conforms to the Shape interface, but that isn't an option unless we have the toolkit's source code. Even if we did, it wouldn't make sense to change ````TextView````; the toolkit shouldn't have to adopt domain-specific interfaces just to make one application work.

Instead, we could define ````TextShape```` so that it adapts the ````TextView```` interface to Shape's. We can do this in one of two ways:
1) by inheriting Shape's interface and ````TextView````'s implementation or
2) by composing a ````TextView```` instance within a ````TextShape```` and implementing ````TextShape```` in terms of ````TextView````'s interface. These two approaches correspond to the class and object versions of the Adapter pattern. 

We call ````TextShape```` an adapter.

![](https://i.imgur.com/wXtL3uI.png)

This diagram illustrates the object adapter case. It shows how BoundingBox requests, declared in class Shape, are converted to GetExtent requests defined in ``TextView``.

Since ``TextShape`` adapts ``TextView`` to the Shape interface, the drawing editor can reuse the otherwise incompatible ``TextView`` class.

Often the adapter is responsible for functionality the adapted class doesn't provide. The diagram shows how an adapter can fulfill such responsibilities. The user should be able to "drag" every Shape object to a new location interactively, but ``TextView`` isn't designed to do that. ``TextShape`` can add this missing functionality by implementing Shape's CreateManipulator operation, which returns an instance of the appropriate Manipulator subclass.

Manipulator is an abstract class for objects that know how to animate a Shape in response to user input, like dragging the shape to a new location. There are subclasses of Manipulator for different shapes; TextManipulator, for example, is the corresponding subclass for ``TextShape``. By returning a TextManipulator instance, ``TextShape`` adds the functionality that ``TextView`` lacks but Shape requires.

### <mark style="background: #69E7E4;">Applicability:</mark>

Use the Adapter pattern when
- you want to use an existing class, and its interface does not match the one you need.
- you want to create a reusable class that cooperates with unrelated or unforeseen classes, that is, classes that don't necessarily have compatible interfaces.
- (object adapter only) you need to use several existing subclasses, but it's impractical to adapt their interface by subclassing every one. An object adapter can adapt the interface of its parent class.

### <mark style="background: #69E7E4;">Structure:</mark>

A class adapter uses multiple inheritance to adapt one interface to another:
![](https://i.imgur.com/5ttESPH.png)

### <mark style="background: #69E7E4;">Participants:</mark>

<mark style="background: #69E7E4;">Target</mark> (``Shape``) - defines the domain-specific interface that Client uses.

<mark style="background: #69E7E4;">Client</mark> (``DrawingEditor``) - collaborates with objects conforming to the Target interface.

<mark style="background: #69E7E4;">Adaptee</mark> (``TextView``) - defines an existing interface that needs adapting.

<mark style="background: #69E7E4;">Adapter</mark> (``TextShape``) - adapts the interface of Adaptee to the Target interface.

<mark style="background: #69E7E4;">Collaborations</mark> - Clients call operations on an Adapter instance. In turn, the adapter calls Adaptee operations that carry out the request.

### <mark style="background: #69E7E4;">Consequences:</mark>

Class and object adapters have different trade-offs. 

<mark style="background: #69E7E4;">A class adapter:</mark>
- adapts Adaptee to Target by committing to a concrete Adapter class. As a consequence, a class adapter won't work when we want to adapt a class and all its subclasses.
- lets Adapter override some of Adaptee's behaviour, since Adapter is a subclass of Adaptee.
- introduces only one object, and no additional pointer indirection is needed to get to the Adaptee.

<mark style="background: #69E7E4;">An object adapter:</mark>
- lets a single Adapter work with many Adaptees—that is, the Adaptee itself and all of its subclasses (if any). The Adapter can also add functionality to all Adaptees at once.
- makes it harder to override Adaptee behaviour. It will require subclassing Adaptee and making Adapter refer to the subclass rather than the Adaptee itself.

### <mark style="background: #69E7E4;">Issues to consider when using the Adapter pattern:</mark>

1. <mark style="background: #69E7E4;">How much adapting does Adapter do?</mark> Adapters vary in the amount of work they do to adapt Adaptee to the Target interface. There is a spectrum of possible work, from simple interface conversion — for example, changing the names of operations—to supporting an entirely different set of operations. The amount of work Adapter does depends on how similar the Target interface is to Adaptee's.
2. <mark style="background: #69E7E4;">Pluggable adapters</mark>. A class is more reusable when you minimize the assumptions other classes must make to use it. By building interface adaptation into a class, you eliminate the assumption that other classes see the same interface. Put another way, interface adaptation lets us incorporate our class into existing systems that might expect different interfaces to the class. ObjectWorks\Smalltalk [Par90] uses the term pluggable adapter to describe classes with built-in interface adaptation.
 
Consider a ``TreeDisplay`` widget that can display tree structures graphically. If this were a special-purpose widget for use in just one application, then we might require the objects that it displays to have a specific interface; that is, all must descend from a Tree abstract class. But if we wanted to make ``TreeDisplay`` more reusable (say we wanted to make it part of a toolkit of useful widgets), then that requirement would be unreasonable. Applications will define their own classes for tree structures. They shouldn't be forced to use our Tree abstract class. Different tree structures will have different interfaces.

 In a directory hierarchy, for example, children might be accessed with a ``GetSubdirectories`` operation, whereas in an inheritance hierarchy, the corresponding operation might be called ``GetSubclasses``. A reusable ``TreeDisplay`` widget must be able to display both kinds of hierarchies even if they use different interfaces. In other words, the ``TreeDisplay`` should have interface adaptation built into it.

# <mark style="background: #69E7E4;">09. Evolutionary Architecture and Emergent Design</mark>

 
### <mark style="background: #69E7E4;">Summary:</mark>

Software architecture and design generate a lot of conversational heat but not much light. 

To start a new conversation about alternative ways to think about them, this article launches the [Evolutionary architecture and emergent design](http://www.ibm.com/developerworks/views/java/libraryview.jsp?search_by=evolutionary+architecture+emergent+design:) series. 

Evolutionary architecture and emergent design are agile techniques for deferring important decisions until the last responsible moment.

In this introductory instalment, series author Neal Ford defines architecture and design and then identifies overarching concerns that will arise throughout the series.

### <mark style="background: #69E7E4;">Defining Architecture:</mark>

- Still have only vague definitions for it
- When we discuss architecture, we're really talking about several different but related concerns that generally fall into the broad categories of <mark style="background: #69E7E4;">application architecture</mark> and <mark style="background: #69E7E4;">enterprise architecture</mark>

### <mark style="background: #69E7E4;">Application Architecture:</mark>

Application architecture describes the coarse-grained pieces that compose an application
 
In the Java world, for example, application architecture describes two things:     
- the combination of frameworks used to build a particular application, which may be called the <mark style="background: #69E7E4;">framework-level architecture</mark>
- the more traditional logical separation of concerns

Object-oriented practitioners have discovered that individual classes don't work well as a reuse mechanism, hence separate out framework architecture

### <mark style="background: #69E7E4;">Application Architecture & Frameworks:</mark>

The unit of reuse in modern object-oriented languages is the library or framework    

When you start a new project in framework-rich languages like the Java language, one of the first architectural concerns is the application's framework-level architecture

Could say Java has become a framework-oriented language    

Framework-level architecture represents a physical architecture, described by specific building blocks

### <mark style="background: #69E7E4;">Application Architecture:</mark>

How do the logical pieces of the application fit together?

This is the realm of design patterns and other structural descriptions, and thus tends to be both more abstract and logical rather than physical    

For example, you can say that a Web application adheres to the Model-View-Presenter pattern without specifying which framework you use to achieve that logical arrangement

### <mark style="background: #69E7E4;">Enterprise Architecture:</mark>

Concerned itself with how the enterprise as a whole uses applications 

Application architecture likens enterprise to city planning and application to building architecture

Enterprise architecture has gotten a lot of attention because of Service-Oriented Architecture (SOA)

SOA blurs the lines between enterprise and application architecture when it dictates characteristics of application construction

### <mark style="background: #69E7E4;">Extant Definitions:</mark>

Superficial so far, need to be more nuanced

Fowler reports “The RUP, working off the IEEE definition, defines architecture as 'the highest level concept of a system in its environment. The architecture of a software system (at a given point in time) is its organization or structure of significant components interacting through interfaces, those components being composed of successively smaller components and interfaces.’”

Fits within the realm of application architecture described above. While vague, it does capture the essence of architecture's responsibility: the highest-level concept.

### <mark style="background: #69E7E4;">Extant Definitions:</mark>

Johnson says "A better definition would be: 'In most successful software projects, the expert developers working on that project have a shared understanding of the design system design. This shared understanding is called "architecture." This understanding includes how the system is divided into components and how the components interact through interfaces.'“

Software development relies on communication more than technology

Architecture really represents the shared knowledge about the system, not technological ephemera

Fowler himself provides a good succinct definition of architecture: "Architecture is about the important stuff. Whatever that is." 

What's important to business analysts differs from the important stuff for an enterprise architect

Or yet another: "Stuff that's hard to change later."  fits best into the idea of an evolutionary architecture

A core idea behind evolutionary architecture is to defer decisions as late as you can, which allows you to substitute alternatives that recent experience has shown are superior

### <mark style="background: #69E7E4;">Defining Design:</mark>

Represents the nuts and bolts of how a piece of software goes together

Encompasses well-trodden territory such as design patterns, refactoring, frameworks, and other daily developer concerns

Design roughly falls on a spectrum between <mark style="background: #69E7E4;">BDUF</mark> (Big Design Up Front) and Cowboy Hacking

BDUF suggests that you can anticipate all the hundreds and thousands of concerns that pop up when you develop software and tries to limit your responses to them

![](https://i.imgur.com/7ZbtEqO.png)

### <mark style="background: #69E7E4;">Architectural and Design Concerns:</mark>

Why the distinction between <mark style="background: #69E7E4;">evolutionary</mark> and <mark style="background: #69E7E4;">emergent</mark>? 

Emergent architecture not a good idea. If you accept that architecture is about things hard to change later, it becomes difficult to allow an architecture to emerge.

Architecture concerns infrastructure elements that must exist before you can start the application. However, just because you can't allow architecture to emerge doesn't mean that it can't <mark style="background: #69E7E4;">evolve</mark>. 

If you have created a flexible architecture and taken care not to create an irreversible decision, you can allow it to evolve over time as new concerns appear.

### <mark style="background: #69E7E4;">Principal and Interest - Technical Debt:</mark>

<mark style="background: #69E7E4;">Technical debt:</mark> make compromises in design for the sake of some external force, such as schedule pressure

Hack a just-in-time solution and hope to use some future time to come back and retrofit it

Compromises made now for the sake of expediency cause <mark style="background: #69E7E4;">entropy</mark> (measure of complexity) to build up in your software and a price will have to be paid for that for the remaining life of the project
 
Can think of inherent complexity as the principal, and the extra effort imposed by previous expedient shortcuts as the interest

### <mark style="background: #69E7E4;">Technical Debt and Interest:</mark>

![](https://i.imgur.com/5mm59HX.png)

### <mark style="background: #69E7E4;">Essential versus Accidental Complexity:</mark>

Problems solved in software have an inherent complexity, which may be called <mark style="background: #69E7E4;">essential</mark> complexity
 
<mark style="background: #69E7E4;">Accidental</mark> complexity arises from the compromises made that incur technical debt. Externally imposed ways that software becomes complex

Payroll example with extra day off in one factory only adds essential complexity as it is part of business rules  

Accidental complexity:
- Just in time hacking
- Pure plumbing exercises like the first two versions of Enterprise JavaBeans (EJB. A few projects need the extra overhead introduced by these tools, but they do nothing but add complexity to most of the projects that use them.

Three things tend to spawn accidental complexity
- just-in-time hacks
- Duplication is the single most insidious diminishing force in software development
	- Can arise from copy-and-paste
	- Object-relational mapping tool tend to have lots of duplication. Database schema, the XML mapping file, and the backing POJOs have slightly different but overlapping information. 
    
- The third enabler of accidental complexity is <mark style="background: #69E7E4;">irreversibility</mark>. Any decision made that cannot be reversed will eventually lead to some level of accidental complexity.

- Irreversibility affects both architecture and design, although its effects are both more common and more damaging at the architectural level.

### <mark style="background: #69E7E4;">Principle of Last Responsible Moment:</mark>

What can I do to allow me to defer that decision?

E.g. distinction made earlier between framework-level architecture and application architecture

Suppose you know that you want the separation of concerns of Model-View-Presenter   

Too often the leap to a physical implementation of that logical architecture by choosing a framework that meets some or all of the requirements

### <mark style="background: #69E7E4;">Rampant Genericness:</mark>

Overengineering solutions by trying to make them as generic as possible – common in Java world

Build in lots of layers for extension, and later more functionality can be more easily built  

Dangerous trap as genericness adds entropy or complexity

Damage your ability to evolve the design in interesting ways early in the project

Adding too much flexibility makes every change to the code base more complex

Planning for the project to live as long as possible truncated its life

YAGNI  is an Agile Approach - just implement exactly what you need now, and if you need more stuff later, you can add it then

How to navigate the fine line between extensibility and overengineering is difficult

# <mark style="background: #69E7E4;">11. Intro to Software Testing</mark>

 
### <mark style="background: #69E7E4;">Role of Testing:</mark>

Testing is basic to every engineering discipline
- Design a drug
- Manufacture an airplane
- Etc.

Why?
- Because our ability to predict how our creations will behave is imperfect
- We need to check our work, because we will make mistakes

### <mark style="background: #69E7E4;">Testing and development of Software</mark>

In what way is software different?

Folklore:
- “Optimism is the occupational hazard of programming; testing is the treatment”
- The implication is that programmers make poor testers

### <mark style="background: #69E7E4;">Why Test?</mark>

![](https://i.imgur.com/AMHqRZp.png)
![](https://i.imgur.com/Kywd6Ra.png)

### <mark style="background: #69E7E4;">Typical Scenario:</mark>

![](https://i.imgur.com/Bo2OHJ1.png)

![](https://i.imgur.com/jnDrcG7.png)

![](https://i.imgur.com/9ericrr.png)

![](https://i.imgur.com/kvWlSaj.png)

![](https://i.imgur.com/yZrGkW6.png)

### <mark style="background: #69E7E4;">Software Development Today:</mark>

![](https://i.imgur.com/gh3n4YQ.png)


### <mark style="background: #69E7E4;">Key Assumptions:</mark>

- Human organizations need decision makers to manage (finite) resources (including time)
- Development and testing must be independent

### <mark style="background: #69E7E4;">Independent Testing:</mark>

Programmers have a hard time believing they made a mistake

Plus a vested interest in not finding mistakes

Design and programming are constructive tasks. Testers must seek to break the software

<mark style="background: #69E7E4;">Wrong Conclusions:</mark>
- The developer should not be testing at all (Recall “test before you code”)
- Testers only get involved once software is done
- Toss the software over the wall for testing(Testers and developers collaborate in developing the test suite)
- Testing team is responsible for assuring quality (Quality is assured by a good software process)

### <mark style="background: #69E7E4;">The Purpose of Testing:</mark> 

Two purposes:
- Find bugs. Find important bugs.
- Elucidate the specification: When testing the prototype or strawman

### <mark style="background: #69E7E4;">Example:</mark>

Test case: Add a child to Mary Brown’s record

- Version 1
	- Check that Ms. Brown’s # of children is one more
- Version 2
	- Also check Mr. Brown’s # of children
- Version 3
	- Check that no one else’s child counts changed

### <mark style="background: #69E7E4;">Specifications:</mark>

- Good testers clarify the specification: This is creative, hard work
- There is no hope tools will automate this: This part will stay hard work

### <mark style="background: #69E7E4;">Testing Strategies:</mark>

![](https://i.imgur.com/rgsBSbY.png)

### <mark style="background: #69E7E4;">V model:</mark>

![](https://i.imgur.com/7mk6MrF.png)

![](https://i.imgur.com/AS9jSwv.png)

![](https://i.imgur.com/MwWQrxE.png)

### <mark style="background: #69E7E4;">Unit tests:</mark>

Focus on smallest unit of design:
- A procedure, 
- a class,
- a component

Test the following:
- Local data structures
- Basic algorithm
- Boundary conditions
- Error handling

May need drivers and stubs
Good idea to plan unit tests ahead

### <mark style="background: #69E7E4;">Integration Testing:</mark>

- If all parts work, how come the whole doesn’t?

- For software, the whole is more than the sum of the parts
	- Individual imprecision is magnified
	- Unclear interface design
	
- Don’t try the “big bang” integration !
- Do incremental integration
	- Top-down integration
	- Bottom-up integration

### <mark style="background: #69E7E4;">Unit vs. Integration Testing:</mark>

![](https://i.imgur.com/F6Y98A5.png)

### <mark style="background: #69E7E4;">Top-Down Integration:</mark>

- Test the main control module first
- Slowly replace stubs with real code
	- Can go depth-first, along a favourite path, to create a working system quickly
	- Or, breadth first
- Problem: you may need complex stubs to test higher-levels

### <mark style="background: #69E7E4;">Bottom-Up Integration:</mark>

- Integrate already tested modules
- No stubs, but need drivers. Often the drivers are easier to write
- Example:
	- Financial code that depends on subroutine for computing roots of polynomials
	- We cannot test the code without the subroutine. A simple stub might not be enough
	- We can develop and test the subroutine first.

- Plan for testability !

### <mark style="background: #69E7E4;">Validation Testing:</mark>

- Culmination of integration testing and functional testing: The software works, but does it do what we need?
- <mark style="background: #69E7E4;">Run acceptance tests:</mark> Get your customer to define them
- <mark style="background: #69E7E4;">Alpha-testing</mark> (in controlled environment): With developer looking over the shoulder
- <mark style="background: #69E7E4;">Beta-testing:</mark> At end-user sites

### <mark style="background: #69E7E4;">Other forms of High-Level Testing:</mark>

- System testing: Involves non-software components
- Security testing: Red-team testing
- Performance testing: E.g., real-time systems
- Stress testing ...

### <mark style="background: #69E7E4;">Stress Testing:</mark>

Push system into extreme situations and see if it still works . . .

<mark style="background: #69E7E4;">Stress:</mark>
- Performance: Feed data at very high, very low rates
- Interfaces: Replace APIs with badly behaved stubs
- Internal structures: Works for any size array? Try sizes 0 and 1.
- Resources: Set memory artificially low. Same for # of file descriptors, network connections, etc.

Stress testing will find many obscure bugs. Explores the corner cases of the design: “Bugs lurk in corners, and congregate at boundaries”

Some may not be worth fixing: Too unlikely in practice

A corner case now is tomorrow’s common case
- Data rates, data sizes always increasing
- Your software will be stressed

### <mark style="background: #69E7E4;">Assertions:</mark>

Use <mark style="background: #69E7E4;">assert(...)</mark> liberally
- Documents important invariants
- Makes your code self-checking
- And does it on every execution!

Opinion: Most programmers don’t use assert enough

### <mark style="background: #69E7E4;">A Problem:</mark>

Testing is weak: Can never test more than a tiny fraction of possibilities

Testers don’t know as much about the code as
the developers, but developers can only do so much testing

What can we do?

### <mark style="background: #69E7E4;">Code Inspections:</mark>

Here’s an idea: Understand the code!

One person explains to a group of programmers how
a piece of code works

<mark style="background: #69E7E4;">Key points:</mark>
- Don’t try to read too much code at one sitting
- A few pages at most
- Everyone comes prepared
- Distribute code beforehand
- No blame
- Goal is to understand, clarify code, not roast programmers

### <mark style="background: #69E7E4;">Experience with Inspections:</mark>

Inspections work!
- Finds 70%-90% of bugs in studies
- Dramatically reduces cost of finding bugs

<mark style="background: #69E7E4;">Other advantages:</mark>
- Teaches everyone the code
- Finds bugs earlier than testing

<mark style="background: #69E7E4;">Bottom line:</mark> More than pays for itself

### <mark style="background: #69E7E4;">Manual Testing:</mark>

Test cases are lists of instructions - “test scripts”

Someone manually executes the script and does each action, step-by-step
- Click on “login”
- Enter username and password
- Click “OK”
- ...

And manually records results

Low-tech, simple to implement

Manual testing is very widespread
- Probably not dominant, but very, very common

Why? Because:
- Some tests can’t be automated (Usability testing)
- Some tests shouldn’t be automated (Not worth the cost)

Those are the <mark style="background: #69E7E4;">best reasons</mark>

There are also <mark style="background: #69E7E4;">not-so-good reasons</mark>:
- Not-so-good because innovation could remove them
- Testers aren’t skilled enough to handle automation
- Automation tools are too hard to use
- The cost of automating a test is 10x doing a manual test

### <mark style="background: #69E7E4;">Automated Testing:</mark>

Idea:
- Record manual test
- Play back on demand

This doesn’t work as well as expected, E.g., Some tests can’t/shouldn’t be automated

### <mark style="background: #69E7E4;">Fragility:</mark>

Test recording is usually very fragile:
- Breaks if environment changes anything
- E.g., location, background colour of textbox

More generally, automation tools cannot generalise:
- They literally record exactly what happened
- If anything changes, the test breaks

A hidden strength of manual testing:
- Because people are doing the tests, ability to adapt tests to slightly modified situations is built-in

### <mark style="background: #69E7E4;">Breaking Tests:</mark>

When code evolves, tests break:
- E.g., change the name of a dialog box
- Any test that depends on the name of that box breaks

Maintaining tests is a lot of work
- Broken tests must be fixed; this is expensive
- Cost is proportional to the number of tests
- Implies that more tests is not necessarily better

### <mark style="background: #69E7E4;">Improved Automated Testing:</mark>

Recorded tests are too low level:
- E.g., every test contains the name of the dialog box

Need to abstract tests:
- Replace dialog box string by variable name X
- Variable name X is maintained in one place So that when the dialog box name changes, only X needs to be updated and all the tests work again

This is just structured programming: Just as hard as any other system design

### <mark style="background: #69E7E4;">Regression Testing:</mark>

Idea:
- When you find a bug,
- Write a test that exhibits the bug,
- And always run that test when the code changes,
- So that the bug doesn’t reappear 

Without regression testing, it is surprising how often old bugs reoccur

Regression testing ensures forward progress: We never go back to old bugs

Regression testing can be manual or automatic: Ideally, run regressions after every change to detect problems as quickly as possible

But, regression testing is expensive
- Limits how often it can be run in practice
- Reducing cost is a long-standing research problem

Other tests (besides bug tests) can be checked for regression
- Requirements/acceptance tests
- Performance tests

Ideally, entire suite of tests is rerun on a regular basis to assure old tests still work

### <mark style="background: #69E7E4;">Nightly Build:</mark>

Build and test the system regularly: Every night

Why? Because it is easier to fix problems earlier
- Easier to find the cause after one change than after 1,000
- Avoids new code from building on the buggy code

Test is usually subset of full regression test
- “smoke test”
- Just make sure there is nothing horribly wrong

### <mark style="background: #69E7E4;">Discussion:</mark>

Testers have two jobs:
- Clarify the specification
- Find (important) bugs

Only the latter is subject to automation

Helps explain why there is so much manual testing

Nevertheless, automate as much as you can

### <mark style="background: #69E7E4;">Back to Design:</mark>

Testing has a profound impact on design because some designs are easier to test.

Design software so it can be tested!

Or at least avoid designing software that cannot be tested

### <mark style="background: #69E7E4;">Principles of Testability:</mark>

Avoid unpredictable results

No unnecessary non-deterministic behaviour

Design in self-checking

At appropriate places have system check its own work (Asserts)

May require adding some redundancy to the code

### <mark style="background: #69E7E4;">Principles of Testabilty:</mark>

<mark style="background: #69E7E4;">Avoid system state:</mark>
- System retains nothing across units of work: A transaction, a session, etc.
- System returns to well-known state after each task is complete: Easiest system to test

Minimize interactions between features:
- Number of interactions can easily grow huge
- Rich breeding ground for bugs

Have a test interface

### <mark style="background: #69E7E4;">Testing Frameworks:</mark>

Key components of a test system are
- Building the system to test (May build many different versions to test)

Running the tests

Deciding whether tests passed/failed )Sometimes a non-trivial task, e.g., compilers)

Reporting results

Testing frameworks provide these functions – E.g. JUnit

### <mark style="background: #69E7E4;">Summary:</mark>

Testing requires a certain mindset

Want to break the code

Good testing is hard work:
- Requires real insight into the nature of the system
- Will help elucidate the spec
- Early Phase of Development
- 
- <mark style="background:#69E7E4;">Inputs:</mark>
    - Informal Specification
	
- <mark style="background:#69E7E4;">Activities:</mark>
    - Create use case model
    - Define use cases
    - Create domain model
    - Create Glossary
    
- <mark style="background:#69E7E4;">Restaurant System (Example):</mark>
    
    - Current System uses physical booking sheets
    
    - <mark style="background:#69E7E4;">Current Functionality:</mark>
        
        - Advance bookings are recorded on sheets
            - Name and phone number of contact
            - Number of diners: ("covers")
            
        - 'Walk-ins' also recorded:
            - Number of covers only
            
        - Bookings allocated to a table
        - Cancellations, etc., are recorded physically on the booking sheet
        
    
- <mark style="background:#69E7E4;">Define First Iteration:</mark>
    
    - First iteration should implement the minimal useful system
    
    - <mark style="background:#69E7E4;">Basic functionality:</mark>
        - Record bookings
        - Update booking sheet information
        
    - System could then replace manual sheets
    
- <mark style="background:#69E7E4;">Use Case view:</mark>
    
    - This view is intended to provide a structured view of the system's functionality
    - Based round a description of how users interact with the system
    - Supported by UML use case diagrams
    - Serves as the starting point for all subsequent development
    
- <mark style="background:#69E7E4;">Use Cases:</mark>
    - The different tasks that users can perform while interacting with the system
        
    - Preliminary list for booking system:
    - record information about a new booking
    - cancel a booking
    - record the arrival of a customer
    - move a customer from one table to another
    
- <mark style="background:#69E7E4;">Actors:</mark>
    
    - Actors are the roles users play when interacting with a system, e.g.:
        - Receptionist (makes bookings)
        - Head waiter (assigns tables etc.)
    
    - Individual users may play one or more role at different times
    - Customers are not users of the system, hence not recorded as an actor
    
- <mark style="background:#69E7E4;">Use Case Diagrams:</mark>
    
    - Show use cases, actors and who does what
    - ![](local://C:/Users/dervl/remnote/remnote-644bbf51117a5271f76257fc/files/_ZZh-CsoJswMPiOKZP8pCnd_9vQalrFf-gOvMrgSc-KUiJ88m8XYdKKSWF8H7Qwzep891nVmOUBxTqYOHIEY1a0TIqUQLwJa-eKx0w8yBBo6Ea8o3wsUq8YZsn0Xr7m2.png)
    
- <mark style="background:#69E7E4;">Describing Use Cases:</mark>
    
    - A use case comprises all the possible interactions that a user can have when performing a given task
    - These are described as courses of events, or scenarios
    
    - A full description of a use case includes:
        - a basic course of events
        - an number of alternative and exceptional courses
        
    
- <mark style="background:#69E7E4;">Basic Course of Events:</mark>
    
    - This describes what happens in the ‘normal’ case
    
    - For example, for ‘Record Booking’:
        - receptionist enters date
        - system displays bookings
        - receptionist enters details
        - system records and displays new booking
    
    - Often a dialogue between system and user
    
- <mark style="background:#69E7E4;">Alternative course of events:</mark>
    
    - Describe predicted alternative flows
    - For example, if no table is available:
        - receptionist enters date
        - system displays bookings
        - no table available: end of use case
        
    
- <mark style="background:#69E7E4;">Exceptional Courses of Events:</mark>
    
    - Situations where a mistake has been made
    
    - E.g. allocate a booking to a small table
        - receptionist enters date
        - system displays bookings
        - receptionist enters details
        - system asks for confirmation of oversize booking
        - if “no”, use case terminates with no booking made
        - if “yes”, booking recorded with warning flag
        
    
- <mark style="background:#69E7E4;">Use case templates:</mark>
    
    - UML does not define a standard format for use case descriptions
    - Various templates have been defined to structure descriptions
    - Essentially a list of subheadings such as:
        - name
        - actors
        - courses of events
        
    
- <mark style="background:#69E7E4;">User-interface Prototype:</mark>
    
    - When writing use cases, it is useful to have a rough idea of the planned user interface
    - ![](local://C:/Users/dervl/remnote/remnote-644bbf51117a5271f76257fc/files/Xf8DJdTHGeh883dZW8V25NaCBdVDxpiom5UEADPVQT22ZG25GMl7leUXKU2EEqQLDbQ3blBViYrIkmIohAC4eWRzCjVdf5T97AiaVn0i5QAwYKNTTinGNYO5fYyrwuQG.png)
    
- <mark style="background:#69E7E4;">Shared Functionality:</mark>
    
    - Different use cases can overlap
    
    - E.g. ‘Record Arrival’:
        - head waiter enters date
        - system displays bookings
        - head waiter confirms arrival for booking
        - system records this and updates display
    
    - First two steps shared with ‘Record Booking’ (even though different actor)
    
- <mark style="background:#69E7E4;">Use Case Inclusion:</mark>
    
    - Move shared functionality to a separate use case, eg ‘Display Bookings’:
        - user enters a date
        - system displays bookings for that date
        
    - Include this in other use cases:
        - receptionist performs ‘Display Bookings’
        - receptionist enters details
        - system records and displays new booking
        
    
- <mark style="background:#69E7E4;">The 'include' Dependency:</mark>
    
    - UML shows inclusion as a dependency between use cases, labelled with the stereotype include:
    - ![](local://C:/Users/dervl/remnote/remnote-644bbf51117a5271f76257fc/files/TWJL1G8S5TePzoZ7gg1C9FmoF9buF1YNCfgPgm1jCJ8B8pgHdShbSsIspH0gzWieYK3h84X1hojymSlCr7HZArqXYx-Sm3m5I75BU1q3oCdc-j_rZN7nrjpPEkqGNtBW.png)
    
- <mark style="background:#69E7E4;">Actor Generalisation:</mark>
    
    - This diagram shows that the receptionist can display bookings without performing the including use case ‘Record Booking’
    - Head waiters can also display bookings
    - Introduce a more general actor to show what the other two actors have in common
    - The initial actors are specialisations of the general actor
    - ![](local://C:/Users/dervl/remnote/remnote-644bbf51117a5271f76257fc/files/1HEahbzYHOJChwvooEGOKA7pZDyqQ76EFt-waiIGFl3UzfGlV6OHCjaIfuMYYbWigHJUfI0uZgj-lvtgb9frJiA-TZTeVF75Z2hwMGSPCwCwcavtbbPjJK6aZt7t3bFd.png)
    
- <mark style="background:#69E7E4;">Use Case Extension:</mark>
    
    - Recording a walk-in can be described as an exceptional source of events
        - someone arrives but there’s no booking recorded
        
    - It could also be a separate use case
        - a customer arrives and asks if there's a free table
        
    - Then it can extend ‘Record Arrival’
        - even without a booking, the customer stays to eat
        
    
- <mark style="background:#69E7E4;">Complete Use-Case Diagram:</mark>
    
    - ![](local://C:/Users/dervl/remnote/remnote-644bbf51117a5271f76257fc/files/_kI3PIaZqr42mq7SR2uyXFZROTmjriyNrAj8XhobEOcny-XSTwAuVYel6YADYfIHapO16KLS7zlt-Fp8AQLLDpKgj2fJ3LQMaspbLvDgR5fhCwE6AD3zAQGbMAI7h2WW.png)
    
- <mark style="background:#69E7E4;">Domain Modelling:</mark>
    
    - Using UML to construct a model of the real-world system
        - similar to entity-relationship modelling
        
    - Model recorded as a class diagram
    - ‘Seamless development’
        - same notation used for analysis and design
        - design can evolve from initial domain model
        
    
- <mark style="background:#69E7E4;">Domain Model Notation:</mark>
    
    - Subset of class diagram notation
        - <mark style="background:#69E7E4;">classes</mark> represent real-world entities
        - <mark style="background:#69E7E4;">associations</mark> represent relationships between the entities
        - <mark style="background:#69E7E4;">attributes</mark> represent the data held about entities
        - <mark style="background:#69E7E4;">generalisation</mark> can be used to simplify the structure of the model
        
    
- <mark style="background:#69E7E4;">Customers and Reservations:</mark>
    
    - Basic business fact: customers make reservations
    - ![](local://C:/Users/dervl/remnote/remnote-644bbf51117a5271f76257fc/files/Ki7C1la-R8uaGVUJ2W_pBX4ZL72wif2jaFjtla-2lTDGZqueWvJTEPgk_T30uDi4Sx11DYhBDYGmzXFRTo6Eaqm6xn3rOFkbTFC_mpePZon-E0aUbTnuh-Bi83qFCrE5.png)
    
- <mark style="background:#69E7E4;">Defining a Relationships:</mark>
    
    - Give a name to the relationship
        - use a verb so that the relationship can be read as a sentence
        
    - A customer can make many reservations
    - How many people make a reservation?
        - one principal contact whose details are held
        - the expected number of diners can be modelled as an attribute of the reservation
        
    
- <mark style="background:#69E7E4;">Tables:</mark>
    
    - Is table number an attribute of ‘Reservation’?
    - Better modelled as a separate class
        - tables exist even if there are no reservations
        - other attributes of tables, e.g. size, can be stored
        
    - ![](local://C:/Users/dervl/remnote/remnote-644bbf51117a5271f76257fc/files/d1suaOp7LfB62yusND4RmLHxCzn5zOD2G3UsvyzLEKCQJQe62zmjxEZSRDE-TSqKPFC7e5u1nbxJea4u2EGSkSLjiDHNS7Krna_W-AEWulIytIzy5sokdtPo0FVCmKJW.png)
    
- <mark style="background:#69E7E4;">Constraints:</mark>
    
    - Not all domain properties can be shown graphically
        - e.g. it should be impossible to double-book a table
        
    - Constraints add information to models
    - written in a note connected to the model element being constrained
    
- <mark style="background:#69E7E4;">Use of Generalisation:</mark>
    - A superclass can be used to show the properties shared by different types of booking
    - ![](local://C:/Users/dervl/remnote/remnote-644bbf51117a5271f76257fc/files/GQEKA-iucChRXPdJPxrfXag2IK2Jh1u06ACtQlmph8MerhBHpC1ieUPj4crBSbHUvVW73hQ5mCcEPI8FNY5cQ2avS9URqjJbkGBjFAp6lrjIN6-tTqYFlDUaSuSbDUfl.png)
    
- <mark style="background:#69E7E4;">Correctness:</mark>
    
    - How do we know when a domain model is complete?
        - we don't: there are lots of plausible models in most cases
        
    - Domain modelling is not an end in itself, but a guide to further development
    - Realizing use cases tests the domain model, and will usually lead to refinements
    
- <mark style="background:#69E7E4;">Glossaries:</mark>
    
    - Domain models capture important system concepts
    - Useful to record these terms and their definitions for use throughout a project
    - Do this in the form of a glossary
    
- <mark style="background:#69E7E4;">Partial restaurant glossary:</mark>
    
    - <mark style="background:#69E7E4;">Booking:</mark> an assignment of diners to a table
    - <mark style="background:#69E7E4;">Covers:</mark> the number of diners for a booking
    - <mark style="background:#69E7E4;">Customer:</mark> a person who makes a reservation
    - <mark style="background:#69E7E4;">Reservation:</mark> a booking made in advance
    - <mark style="background:#69E7E4;">Walk-in:</mark> a booking that is not made in advance
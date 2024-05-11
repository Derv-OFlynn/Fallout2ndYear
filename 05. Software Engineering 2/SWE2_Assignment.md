<h1 style="text-align:center;"><mark style="background: #69E7E4;">Software Engineering 2 Assignment </mark> </h1>
 <h1 style="text-align:center;"><mark style="background: #69E7E4;">Library </mark> </h1>

 <h2 style="text-align:center;"><mark style="background: #69E7E4;">Dervla O'Flynn – C22344363 </mark> </h2>
 

### <mark style="background: #69E7E4;">1. Introduction:</mark>

This is an extension of the USE model of the Library system originating from the Software Engineering 1 module. It includes the new use cases, pre conditions, post conditions, invariants and constraints. It details the State Machine. There are also diagrams included. The use and soil files are also submitted. 

### <mark style="background: #69E7E4;">2. Use Cases Added to the Library System:</mark>

##### <mark style="background: #69E7E4;">reserve():</mark> 

This operation, reserve(), was added to allow a user to reserve a book from the library. Users in real libraries often reserve books and it is a vital part of a functioning library system.

Scenario:
1. User requests reservation
2. The system returns that the user is ok to reserve
3. The book is added to the member's reserved list
4. The copy of the book is added to the library's reserved list

##### <mark style="background: #69E7E4;">payFine():</mark>

This operation allows the member to pay their fine. Libraries impart fines upon users for late fees or losing books. This use case allows them to pay their fine.

Scenario:
1. User requests to pay their fine
3. The user pays the fine
4. The fine is set to 0 on their member account

<mark style="background: #69E7E4;">Code Implementation:</mark>

Member:
![](https://i.imgur.com/4zpN15Q.png)

Copy:
![](https://i.imgur.com/0SLi3cE.png)

<mark style="background: #69E7E4;">Associations:</mark>

![](https://i.imgur.com/5XA6gYh.png)

### <mark style="background: #69E7E4;">3. Preconditions, Post Conditions and Invariants:</mark>

##### <mark style="background: #69E7E4;">Book borrow() operation:</mark>

Pre-condition: the number of copies on the shelf must be greater than 0.
Post-condition: the number of copies on the shelf must be equal to the number there were during the precondition, minus 1.

![](https://i.imgur.com/BdFJFh8.png)

### <mark style="background: #69E7E4;">4. Constraints:</mark>

##### <mark style="background: #69E7E4;">Member borrow() operation:</mark>

Preconditions: The member cannot borrow a book if they already are borrowing a book. The book must be either on the shelf or borrowed by the user already (e.g. extending the borrow period) in order to be borrowed.

Post-conditions: The status of the copy must be "onLoan" and the copy must be borrowed.

![](https://i.imgur.com/m5IkN0s.png)

##### <mark style="background: #69E7E4;">Member reserve() operation:</mark>

Precondition: In order to reserve a copy, the copy must be on the shelf.

Post-condition: The copy's status must be set to "reserved".
![](https://i.imgur.com/HzLdw8i.png)

##### <mark style="background: #69E7E4;">Member return() operation:</mark>

Precondition: In order to return a copy, it must be on loan already.

Post-condition: The copy's status must be set to "onShelf".
![](https://i.imgur.com/SanV99E.png)


#### <mark style="background: #69E7E4;">Testing Constraints:</mark>

Trying to borrow a second book:
![](https://i.imgur.com/7BEdRmL.png)
Success. The user is not allowed to borrow more than 1 book.

Returning a book borrowed by the member:
![](https://i.imgur.com/4h1cx8y.png)
Success. The book is returned.

Returning a book not borrowed by the member:
![](https://i.imgur.com/H81gUT8.png)
Success. The book cannot be returned as is it not borrowed.
### <mark style="background: #69E7E4;">5. State Machine:</mark>

![](https://i.imgur.com/IIRVlCw.png)

### <mark style="background: #69E7E4;">6. Diagrams:</mark>

##### <mark style="background: #69E7E4;">1. Class Diagram</mark>

![](https://i.imgur.com/sx1k5me.png)

##### <mark style="background: #69E7E4;">2. Sequence Diagram</mark>

Reserving a copy, paying a fine and borrowing the copy.
![](https://i.imgur.com/NuuWXc5.png)

Reserving a copy, borrowing the copy and returning the copy.
![](https://i.imgur.com/d41eEZk.png)

##### <mark style="background: #69E7E4;">3. Statemachine Diagram</mark>

Statemachine Diagram for Copy.
![](https://i.imgur.com/6dI5JXG.png)



##### <mark style="background: #69E7E4;">4. Object Diagram</mark>

![](https://i.imgur.com/bRhMFnW.png)


Use Code:

```Java
model Library

class Book
  attributes
    title : String
    author : String
    no_copies : Integer
    no_onshelf : Integer
  operations
    borrow()
    begin
        self.no_onshelf := self.no_onshelf - 1
    end
    pre copiesOnShelf: no_copies >0
    post: no_onshelf = no_onshelf@pre - 1

    return()
    begin
        self.no_onshelf := self.no_onshelf + 1
    end

    reserve()
    begin
        self.no_onshelf := self.no_onshelf - 1
    end

end

class Copy
  attributes
    status : String
  operations
    borrow( m : Member)
    begin
        self.status := 'onLoan';
        self.book.borrow()
    end
    return( m : Member)
    begin
        self.status := 'onShelf';
        self.book.return()
    end
    reserve( m : Member)
    begin
        self.status:= 'isReserved';
        self.book.reserve();
    end


  statemachines
	psm States
	states
		newCopy : initial
		available	[status = 'onShelf']
		taken		[status = 'onLoan']
		reserved	[status = 'isReserved']
	transitions
		newCopy -> available { create }
		available -> taken	{ borrow() }
		available -> reserved { reserve() }
		reserved -> taken { borrow() }
		taken -> available { return() }
	end
end    
    
class Member 
  attributes 
    name : String
    address : String
    no_onloan : Integer
    status : String
    fine : Integer
  operations
    borrow(c : Copy)
    begin
        insert (self, c) into HasBorrowed;
        self.no_onloan := self.no_onloan + 1;
        c.borrow(self);
    end


    return( c: Copy)
    begin
        self.no_onloan := self.no_onloan - 1;
        c.return(self);
        delete (self, c) from HasBorrowed;
    end

    reserve( c: Copy)
    begin
        insert (self, c) into HasReserved;
        c.reserve(self);
    end

    payFine( m :Member)
    begin
        m.fine := 0;
    end
        
end
  

association HasBorrowed between
    Member[0..1] role borrower
    Copy[*] role borrowed
end

association CopyOf between
    Copy[1..*] role copies
    Book[1] role book
end

association HasReserved between
    Member[0..1] role reserver
    Copy[*] role copy
end
  
constraints

context Member::borrow(c:Copy) 
    pre limit: self.no_onloan < 1
    pre: self.borrowed->excludes(c)
    pre: c.status = 'onShelf' or self.copy->includes(c)
    post: c.status = 'onLoan'
    post: self.borrowed->includes(c)


context Member::reserve(c:Copy) 
    pre: c.status = 'onShelf'
    post: self.copy->includes(c)
    post: c.status = 'isReserved'

context Member::return(c:Copy)
    pre: c.status = 'onLoan'
    pre: self.borrowed->includes(c)
    post: c.status = 'onShelf'    
```

Soil File:
```Java
!new Member('Mary')
!Mary.name := 'Mary'
!Mary.no_onloan := 0
!Mary.address := '99 Central Quad'
!Mary.fine := 5
!new Book('Jack_In_The_BeanStalk')
!Jack_In_The_BeanStalk.title := 'Jack_In_The_BeanStalk'
!Jack_In_The_BeanStalk.author := 'Jack'
!new Copy('c1')
!c1.reserved := false
!c1.onLoan := false
!insert(c1,Jack_In_The_BeanStalk) into CopyOf
!new Copy('c2')
!c2.onLoan := false
!c2.reserved := false
!insert (c2,Jack_In_The_BeanStalk) into CopyOf
!Jack_In_The_BeanStalk.no_copies := 2
!Jack_In_The_BeanStalk.no_onshelf := 2
!new Member('Deco')
!Deco.name := 'Declan'
!Deco.no_onloan := 0
!Deco.address := '100 East Quad'
!Deco.fine := 3
!new Copy('c3')
!c3.reserved := false
!c3.onLoan := false
!insert(c3,Jack_In_The_BeanStalk) into CopyOf
!new Book('HumptyD')
!HumptyD.author := 'Humpty'
!HumptyD.title := 'Humpty_Dumpty'
!Deco.reserve(c2)
!Deco.borrow(c2)
!Mary.reserve(c1)
!Mary.borrow(c1)
!Mary.payFine(Mary)
```
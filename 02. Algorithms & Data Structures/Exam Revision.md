#Algo  #ExamPrep 
# <mark style="background: #BD6500;">02. Stacks, Queues and Linked Lists</mark>

<mark style="background:#BD6500;">ADT</mark> stands for <mark style="background:#BD6500;">Abstract Data Type</mark>

### <mark style="background:#BD6500;">ADT Stack:</mark>

<mark style="background:#BD6500;">Node Structure:</mark>
- ![](https://i.imgur.com/u7WhqwJ.png)

```Java
struct Node
{ 
	int data; 
	Node x next; 
}
```
	
### <mark style="background:#BD6500;">Linked List Implementation of a Stack:</mark>

<mark style="background:#BD6500;">Empty Stack:</mark>

- ![](https://i.imgur.com/OL6uYGD.png)

<mark style="background:#BD6500;">Pushing onto empty stack:</mark>

- ![](https://i.imgur.com/8FVCyhN.png)

1.  Create a new linked list node
2. Initialise it
3. Re-point top

```Java
t = new Node;
t->data = x; 
t->next = top; 
top = t;
```

- ![](https://i.imgur.com/8O2GnaV.png)


<mark style="background:#BD6500;">Non-empty Stack:</mark>

- No significant change here. Procedure and code is the same as empty stack.

- ![](https://i.imgur.com/7CRPAk8.png)


<mark style="background:#BD6500;">Array Implementation of Stack:</mark>

- Dynamically create an array of some predefined size when the constructor is called
- ![](https://i.imgur.com/WfD0Ymi.png)


- The code should be quite simple.
- <mark style="background:#BD6500;">NOTE:</mark> pop() is only a valid operation on a non-empty stack

<mark style="background:#BD6500;">StackTest2.java</mark>
```Java
// Array implementation of ADT Stack

 class StackException extends Exception { 
    public StackException(String s) {
        super(s);
    }
}

class Stack {

  private int a[];
  private int top, s_max;
  
  public Stack(){
    top = 0;
	a = new int[4];
	s_max = 4;
  }
  
  public int pop() throws StackException {  
    if(top==0) 
        throw new StackException("\nCARELESS coding: cannot pop empty stack\n");
    int x = a[--top];
	return x;
  }
  
  public void push(int x) throws StackException {
    if(top == s_max) 
	    throw new StackException("\nStack array already full\n");
		 
    a[top++] = x;  
  } 
  
  public void display() {
    int t = 0;
    System.out.println("\nStack contents are:  ");
        
    while (t != top) {            
        System.out.print(a[t] + " ");
        ++t;
    }       
    System.out.println("\n");
  }

}

public class StackTest2
{
    public static void main( String[] arg) //throws Exception 
    {
        Stack s = new Stack();
        System.out.println("Stack is created\n");
        
        // piece of code to test our exception mechanism     
        try {
            s.pop();
        } catch (StackException e){
            System.out.println("Exception thrown: " + e);
        }
        
        try {
            s.push(10); s.push(3); s.push(11); s.push(7);
        } catch( StackException e) {
            System.out.println("Exception thrown: " + e);
        }
        s.display();
		
        try{
            s.push(2);
        } catch(StackException e) {
            System.out.println("Exception thrown: " + e);
        }
        
        s.display();
       
  
    }
}
```

<mark style="background:#BD6500;">StackTest2.java</mark>
```Java
// StackTest.java
// Linked list implementation of Stack

 class StackException extends Exception { 
    public StackException(String s) {
        super(s);
    }
}

class Stack {
       
    class Node {
        int data;
        Node next;  
    }
    private Node top;
      
    public Stack()
    { 
        top = null;
    }
        
    public void push(int x) {
        Node  t = new Node();
        t.data = x;
        t.next = top;
        top = t;
    }

    // only to be called if list is non-empty.
    // Otherwise an exception should be thrown.
    public int pop() throws StackException
    {
        if(this.isEmpty()) 
            throw new StackException("\nIllegal to pop() an empty Stack\n");
        
        int x = top.data;
        top = top.next;
        return x;        
    }

    
    public boolean isEmpty(){
       return top == null;
    }


    public int size() {
        int c = 0;
        Node t = top;
        while(t != null) {
            ++c;
            t = t.next;
        }
        return c;        
    }
    
    public void display() {
        Node t = top;
        //Console.Write("\nStack contents are:  ");
        System.out.println("\nStack contents are:  ");
        
        while (t != null) {            
            System.out.print(t.data + " ");
            t = t.next;
        }       
        System.out.println("\n");
    }

}


public class StackTest
{
    public static void main( String[] arg){
        Stack s = new Stack();
        System.out.println("Stack is created\n");
        
        // piece of code to test our exception mechanism
        try {
            s.pop();
        } catch (StackException e) {
            System.out.println("Exception thrown: " + e);
        }
        
        s.push(10); s.push(3); s.push(11); s.push(7);
        s.display();
        
        System.out.println("Stack sixe is " + s.size());
       
       /* int i = s.pop();
        System.out.println("Just popped " + i);
        s.display();
        */
    }
}
```

<mark style="background:#BD6500;">ADT Queue:</mark>
    
- A queue is a well understood concept in daily life and is also widely used in computing. A queue follows the simple principle of FIFO (first in first out) as opposed to a stack which uses LIFO (last in first out).
- The abstract interface to Queue can be specified in Java by:

```Java
interface Queue 
{
    public:
    void enQueue(int x);
    int deQueue();
    boolean isEmpty();
};
```

- <mark style="background:#BD6500;">StackGeneric.java</mark>
```Java
// StackGeneric.java
// Linked list implementation of a Generic Stack

class Stack<T> {
    
    class Node {
        T data;
        Node next;  
    }
    private Node top;
      
    public Stack()
    { 
        top = null;
    }
        
    public void push(T x) {
        Node  t = new Node();
        t.data = x;
        t.next = top;
        top = t;
    }

    // only to be called if list is non-empty.
    // Otherwise an exception should be thrown.
    public T pop(){
        T y = top.data;
		top = top.next;
		return y;
        
    } 

    
    public boolean isEmpty(){
       return top == null;
    }


    public void display() {
        Node t = top;
        System.out.println("\nStack contents are:  ");
        System.out.println(" top - ");
        while (t != null) {
            System.out.print(t.data + " ");
            t = t.next;
        }
        
        System.out.println("\n");
    }

}

class MyPet {
        public String name;
        public String type ;
        public int age;

        public MyPet(String s, String t, int a) {
            name = s;
            type = t;
            age = a;
        }
        
        public String toString() {
            return "\nI am " + name + " the " + type + ", my age is " + age;
        }
}

public class StackGeneric
{
    public static void main( String[] arg){
        Stack <Integer> s = new Stack <Integer>();
        
        System.out.println("Stack is created\n");
        
        s.push(10); s.push(3);
        s.push(11); s.push(7);
        s.push(23);
        
        s.display();
        
       
        Integer i = s.pop();
        System.out.println("Just popped " + i);
        s.display();
        
		
		Stack <MyPet> s2 = new Stack <MyPet>();
        System.out.println("Stack is created\n");
        
        s2.push(new MyPet("Fluyffy", "cat", 6)); 
        s2.push(new MyPet("Rex", "dog", 3)); 
        s2.push(new MyPet("Lola", "rat", 1)); 
        s2.push(new MyPet("Felix", "cat", 7));
        
        
        s2.display();
        
        MyPet p = s2.pop();
        System.out.println("\nJust popped " + p);
        s2.display(); 
		
    }
}
```

<mark style="background:#BD6500;">Linked List implementation of queues:</mark>
	
- Since new linked list nodes are added to the back of the queue and nodes are removed from the front, it makes sense to use two pointers, head and tail pointing to the first and last node respectively.
- Let us start with adding a value, ``enQueue(x)``, to an initially empty queue. For an empty queue, head points to a dummy node and tail will have a null value.

- <mark style="background:#BD6500;">Empty Queue:</mark>
	- ![](https://i.imgur.com/Y0aleB1.png)
	
	
	1. Create a new node, place x in it
	2. Rearrange pointers to insert x into linked list
	
```Java
t = new Node;
t->data = x;
t->next = z;

if(head == head->next)
{
    head = t;
}
else
{
    tail->next = t;
}
tail = t;     
```
	
<mark style="background:#BD6500;">Non-empty Queue:</mark>
	
- ![](https://i.imgur.com/ialGHrC.png)


1. Create and intialise new node as before
2. Change pointers as shown in diagram

```
t = new Node;
t->data = x;
t->next = z;

if(head == head->next)
{
    head = t;
}
else
{
    tail->next = t;
}
tail = t;  
```
	
- Some of our class code now could look like:

```Java
class Queue 
{
    private class Node 
    {
	int data;
	Node next;
    }
    
    Node z, head, tail;
    
    public Queue() 
    {
        z = new Node(); z.next = z;
        head = z; tail = null;
    }
    
    public void enQueue( int x) 
    {
        Node t;
	t = new Node();
	t.data = x;
	t.next = z;
	
        if(head == z) // case of empty list
        {
	    head = t;
        }
	else // case of list not empty
        {
	    tail.next = t;
        }
	
        tail = t; // new node is now at the tail
    }
	// missing rest of code
}
```

<mark style="background:#BD6500;">Circular Buffer Implementation:</mark>
	
- This is easier to implement than a linked list queue. However, it is not as flexible in terms of memory allocation for growing/shrinking queues

- Example: A buffer of size 4, initially empty
- ![](https://i.imgur.com/Xlc8p9h.png)


- As you can see, when back is incremented after each ``enQueue(x)``, until the end of the buffer is reached. Then if the beginning of the buffer is free, back will go from the end of the buffer to the start. This is easily implemented using modulo arithmetic.

```Java
class Queue 
{
    private:
	int *q, back, front;
	int qmax, size;

    public:
	Queue();
	void enQueue(int x);
	int deQueue();
	bool isEmpty();
};

Queue::Queue( int _qmax) 
{
    qmax = _qmax;
    size = front = back = 0;
    q = new int[qmax];
}
void Queue::enQueue( int x)
{
    if( qmax == size) return;
    q[back] = x;
    back = (back + 1) % qmax;
    ++size;
}
```

# <mark style="background: #BD6500;">03. Priority Queues and Heaps</mark>

### <mark style="background:#BD6500;">Priority Queue:</mark>

- A <mark style="background:#BD6500;">priority queue</mark> is a queue where each element has a priority and the element with the highest priority is at the front of the queue and will be the first element to be removed. To be contrasted with the <mark style="background:#BD6500;">stack</mark> and <mark style="background:#BD6500;">queue</mark> data structures which use <mark style="background:#BD6500;">LIFO</mark> and <mark style="background:#BD6500;">FIFO</mark> respectively

- It can be implemented as an unsorted array or a fully sorted array. Complexities are:
- ![](https://i.imgur.com/rnZwA2u.png)


- So either one has no particular advantage, still get an O(n) operation, i.e. an operation which requires n steps

### <mark style="background:#BD6500;">Binary Tree:</mark>

- A <mark style="background:#BD6500;">binary tree</mark> is a recursive structure where each tree node may have 2 child nodes (or left and right subtrees)

- A <mark style="background:#BD6500;">complete binary tree</mark> is a binary tree where new nodes are added from left to right on the same level and a new level is only added when the current level is full. There are no 'gaps' anywhere in the tree between the first and last nodes

### <mark style="background:#BD6500;">Heap:</mark>

- A <mark style="background:#BD6500;">heap</mark> is another way to implement a <mark style="background:#BD6500;">priority queue</mark>. It has the logical structure of a complete binary tree which satisfies the heap condition

- A <mark style="background:#BD6500;">heap</mark> can be implemented using pointers (each node has 3 pointers - parent, left child and right child) or much more simply using a partially ordered array. In the array implementation where the highest priority key is in array position 1 we have:

```Java
parent(i) = i/2
lchild(i) = 2i 
rchild(i) = 2i + 1
```

- Here, ``parent(i)`` is the array index of the parent of node i

- A heap is <mark style="background:#BD6500;">partially ordered</mark> by satisfying the heap condition

- A fully sorted or ordered array could be used, but this would require more computation to maintain. Heaps make for much more efficient implementation of a priority queue. We will see later that:

- ![](https://i.imgur.com/YJCjKrq.png)


<mark style="background:#BD6500;">Heap Condition:</mark>

- <mark style="background:#BD6500;">Heap condition:</mark> the priority of any node is greater than or equal to that of its left child and right child if it has such child nodes

- <mark style="background:#BD6500;">Example:</mark>

	- ![](https://i.imgur.com/sN1wZJ9.png)


<mark style="background:#BD6500;">Inserting node with key P into the heap:</mark>

- P is added at the bottom right of the tree and sifted up to the correct position

- ![](https://i.imgur.com/KYYcOct.png)


- Finally you end up with:

- ![](https://i.imgur.com/ViJBCPE.png)


- From the point of view of implementing this operation, it is helpful to consider the sift ups from an array perspective

- ![](https://i.imgur.com/VXUhKDJ.png)


- <mark style="background:#BD6500;">Removing largest value X from top of heap:</mark>

    - X is removed and the last value M in the heap is then moved to the top of the heap and <mark style="background:#BD6500;">sifted down</mark>

    - ![](https://i.imgur.com/2t81Sq2.png)


    - ![](https://i.imgur.com/HTWAqRx.png)


    - Finally, M finds the right heap node to stay in

    - ![](https://i.imgur.com/TOKy05N.png)


<mark style="background:#BD6500;">In Summary:</mark>

- ![](https://i.imgur.com/Ps7IJlO.png)


<mark style="background:#BD6500;">Heap Operations in Pseudocode:</mark>

```Java
Key // a type, usually int, describes type of values in heap
int N // number of elements in array or heap
Key a[ ] // heap array of size N containing items of type Key.
The heap array a[] and N will be encapsulated inside the heap object.

insert(Key x)
    a[++N] = x
    siftUp( N)

// siftUp from position k. The key or node value at position k
// may be greater that that of its parent at k/2
// k is a position in the heap array h

siftUp( int k)
    v := a[k]
    a[0] := ∞
    while( v > a[k/2] )
        a[k] := a[k/2]
        k := k/2
    a[k] := v

// Key of node at position k may be less than that of its
// children and may need to be moved down some levels
// k is a position in the heap array h

siftDown(int k)
    v := a[k]
    while( 2k ≤ N ) // while node at pos k has a left child node
    j = 2k
    if( j < N  a[j] < a[j+1])
    ++j
    
    if( v  a[j] ) break
        a[k] = a[j]
        k := j
        a[k] := v

Key remove( )
    a[0] := a[1]
    a[1] := a[N--]
    siftDown( 1)
    return a[0]
```

<mark style="background:#BD6500;">HeapSort Java:</mark>

```Java
class HeapSort {

// used to reform the shrinking heap when
// the largest value is removed.
// N = heap size, a[N-1] is last value on heap
public  static void siftDown( int a[], int k, int n) {
   int v, j;

   v = a[k];
   j = 2*k+1;          // j is position of leftchild of k
   while( j <= n-1) {  // make sure leftchild of k is within the heap
      if(j < n-1 && a[j] < a[j+1]) 
            ++j;
      if( v >= a[j]) 
            break;
      a[k] = a[j];
      k = j;
      j = 2*k + 1;      
   }
   a[k] = v;
}


// in this version, it is assumed the array
// values are a[0] to a[n-1]. Then
// leftChild(k) = 2k+1, nrightChild(k) = 2k + 2
// parent(k) = (k-1)/2

public static void heapSort(int a[], int n)
{
   int k, v;

  // first convert array into heap
   for(k = (n-2)/2; k >= 0; --k)  // parent of last leaf  a[n-1]
      siftDown(a, k, n);     // is at (n-1-1)/2 = n/2 -1

   // repeatedly remove largest value from heap,
   // place in position freed by heap.
   for(k = n-1; k > 0; --k) {
      v = a[0];
      a[0] = a[k];
      siftDown( a, 0, k); // k new heap size
      a[k] = v;
   }
}




public static void main(String arg[])
{
    int a[];
    int N = 10;
    a = new int[N];

    int i;

    // insert 10 random number between 0 and 99 into array
    for(i = 0; i < N; ++i)
       a[i] = (int) (Math.random()*100.0);

    System.out.println( "\nUnsorted array is:\n");
    for(i = 0; i < N; ++i)
        System.out.print("  "  + a[i]);

    HeapSort.heapSort( a, N);

    System.out.println( "\nSorted array is:\n");
    for(i = 0; i < N; ++i)
        System.out.print("  "  + a[i]);
}

}

HeapSort.java
Displaying HeapSort.java.
```

# <mark style="background: #BD6500;">04. Graphs</mark>

- Consider the following <mark style="background:#BD6500;">weighted undirected</mark> (or bidirectional) <mark style="background:#BD6500;">graph</mark>. It could represent a number of different problems such as length or cost of optical fibre between network points, road distances between villages

- ![](https://i.imgur.com/AbtsfvN.png)
  

- In Computer Science there are many useful <mark style="background:#BD6500;">algorithms</mark> that operate on a <mark style="background:#BD6500;">graph data structure</mark> such as:

    - Depth first traversal

    - Breadth first traversal

    - Shortest path tree (3 algorithms, Dijkstra)

    - Minimum spanning tree

    - Hamiltonian cycle

    - Eulerian cycle

- Before any of these are implemented, we first need to consider how a graph such as the one above might be <mark style="background:#BD6500;">stored</mark> or represented in computer <mark style="background:#BD6500;">memory</mark>. Also it makes sense to save it on <mark style="background:#BD6500;">secondary</mark> storage as a text file such as:

    - ![](https://i.imgur.com/IiR3JmQ.png)


- Here, the first row tells us there are 7 vertices and 11 edges. Second row says there is an edge from A to B with weight 7 and vice versa. Third row edge from A to D weight 5 etc

- The simplest way to store this graph in primary memory is to use a 2-D array called an adjacency matrix. We say "adjacency" because it records which vertex is next to or connected to any other vertex

  

### <mark style="background:#BD6500;">Adjacency Matrix:</mark>

- If we use the graph as array indices and call the matrix ``adj[,]`` (or ``adj[][]`` if using Java to style 2D arrays then:

- ``adj[u, v]`` represents the weight of the edge between vertices ``u`` and ``v`` . For example, adj[A,B] or adj[1,2] = 7 and adj[2,1] = 7 . If there is no edge we say adj[u, v] = 0

- ![](https://i.imgur.com/9TnyXIJ.png)


- Here, we have not shown all the matrix values. The complete matrix would be:

- ![](https://i.imgur.com/ExLX1i6.png)


- You can see that for a <mark style="background:#BD6500;">sparse graph</mark> most of the 2-D array would be occupied by 0s. An <mark style="background:#BD6500;">adjacency matrix</mark> is extremely <mark style="background:#BD6500;">inefficient</mark> space-wise for a <mark style="background:#BD6500;">sparse graph</mark>, especially as <mark style="background:#BD6500;">V</mark> (number of vertices) increases

- For <mark style="background:#BD6500;">sparse graphs</mark>, a <mark style="background:#BD6500;">linked list</mark> approach would be a more efficient use of memory as linked list <mark style="background:#BD6500;">nodes</mark> would only be allocated for <mark style="background:#BD6500;">edges</mark> that <mark style="background:#BD6500;">exist</mark>

### <mark style="background:#BD6500;">Adjacency Lists:</mark>

- In this approach, every <mark style="background:#BD6500;">vertex</mark> has a <mark style="background:#BD6500;">linked list</mark> associated with it which only <mark style="background:#BD6500;">records</mark> those vertices <mark style="background:#BD6500;">connected</mark> to it with an edge. The edge <mark style="background:#BD6500;">weights</mark> are also recorded. So, in a bidirectional graph, each edge is represented by <mark style="background:#BD6500;">two linked list nodes</mark>.

- For example, a <mark style="background:#BD6500;">graph constructor</mark> using <mark style="background:#BD6500;">adjacency lists</mark> in the first edge from the above text file would have created an <mark style="background:#BD6500;">array</mark> of <mark style="background:#BD6500;">linked lists</mark> with the following logical structure:

- ![](https://i.imgur.com/Cvksbps.png)


- And after reading 5 edges from the file:

- ![](https://i.imgur.com/t9RAOsr.png)


- On reading all 11 edges:

- ![](https://i.imgur.com/eZxtxye.png)


### <mark style="background:#BD6500;">Graph Traversal Example:</mark>

- Depth first (blue) and breadth first (red)

- Note that the order depends on how the graph is stored, an adjacency matrix may show a DF visiting sequence different to that of an adjacency lists representation

- In this example, we use the adjacency matrix to see which vertices each vertex is connected to

- Also, an extra "visited array" is necessary to prevent an algorithm from visiting a vertex more than once

- ![](https://i.imgur.com/B7pbdYn.png)


<mark style="background:#BD6500;">Graph Search or Traversal:</mark>

- A graph is a complex data structure and can be viewed as a collection on which it may be desirable to do a traversal and process each vertex or edge in some way (similar to the way a <mark style="background:#BD6500;">for loop</mark> can be used to traverse an array)

	- Depth first, may use a stack or recursion

	- Breadth first, uses a queue

	- Best first, uses a priority queue or heap

<mark style="background:#BD6500;">Depth First Traversal:</mark>

- For a connected graph (no isolated nodes), the following algorithm will visit each vertex in depth first fashion. If the graph is disconnected, it will only traverse 1 component of the graph. It easily implemented using recursion. Alternatively, a stack may be used for iterative implementation

```Java
Graph :: DF (Vertex s):
    Begin
        id = 0
        for v = 1 to V
            visited[v] = 0
        dfVisit(0, s)
    End
    
Graph :: dfVisit( Vertex prev, Vertex v)
    Begin
        visited[v] = ++id
        print “Visited vertex “, v, “ along edge “, prev, “—“, v

        foreach vertex u  adj(v)
            if not visited[u]
                dfVisit(v, u)

    End 
```

<mark style="background:#BD6500;">Cormen's Algorithm:</mark>

```Java
DFS(G)
    for each vertex u ∈ G.V
        u.color = white
        u.π = NIL
    
    time = 0
    
    for each vertex u ∈ G.V
        if u.color == WHITE
            DFS_Visit(G, u)
DFS_Visit(G, u)
    time = time + 1 //white vertex u has just been discovered
    u.d = time
    u.color = GRAY
    
    for each v ∈ G.adj[u] //explore edge (u, v)
        if v.colour == WHITE
            v.π = u
            DFS_Visit(G,v)
    
   u.colour = BLACK //blacken u, it is finished
   time = time + 1
   u.f = time  
```

- <mark style="background:#BD6500;">Breadth First Travel:</mark>

```Java
Graph :: BF( Vertex s)
Begin
    Queue q
	
    id = 0

    for v = 1 to V
	visited[v] = 0

    q.enQueue(s)

    while (not q.isEmpty())
	v = q.deQueue()
	if (not visited[v])
	    visited[v] = ++id
	    for each vertex u  adj(v)
	        if (not visited[u])
	            q.enQueue(u)
	    end for
	end if
    end while
End
```

```Java
Graph :: BF( Vertex s)
Begin
    Queue q
	
    id = 0

    for v = 1 to V
	visited[v] = 0

    q.enQueue(s)

    while (not q.isEmpty())
	v = q.deQueue()
	if (not visited[v])
	    visited[v] = ++id
	    for each vertex u  adj(v)
	        if (not visited[u])
	            q.enQueue(u)
	    end for
	end if
    end while
End
```

- Breadth First Traversal (BF) will give a shortest path spanning tree on an unweighted graph. In an unweighted graph, you can consider all edges to have an equal weight of 1. BF visits all the vertices on the same level before proceeding to a "deeper" level, so all vertices newly visited on a level will be the same distance from the starting vertex. Further, since BF proceeds level by level with distances of 0, 1, 2, etc, it will reach a vertex via the shortest path to that vertex.

- If there was another path which was shortest path to a vertex, then the vertex would also belong to another previous level closer to the starting vertex; which of course is a contradiction since any level is exhausted before a deeper one is examined

<mark style="background:#BD6500;">Best First Traversal:</mark>

- This approach attaches a value or priority to each vertex and for each iteration of the while loop, it 'visits' the vertex with the highest priority. The natural auxiliary data structure here is a heap. This method can be used in Minimum Spanning Tree and Shortest Path algorithms

<mark style="background:#BD6500;">Iterative version of Depth First Traversal:</mark>

```Java
Graph :: DF_iter( Vertex start)
Begin
    Stack s
    id = 0
    
    for v = 1 to V
        visited[v] = 0
    
    s.push(start)
    
    while (not s.isEmpty())
        v = s.pop()
        
        if (not visited[v])
            visited[v] = ++id
            
            for each vertex u  adj(v)
                if (not visited[u])
                    s.push(u)

    end while
End
```

# <mark style="background: #BD6500;">05. Minimum Spanning Tree</mark>

# <mark style="background: #BD6500;">Minimum Spanning Tree Algorithms</mark>

- Three well known algorithms, of which we will consider the first two are are due to:
	- Prim
	- Kruskal
	- Borůvka
	
- Given a connected, weighted and undirected graph, a spanning tree of that graph is a subgraph that is a tree and connects all the vertices together. 

- A single graph can have many different spanning trees. 

- The weight of a spanning tree is obtained by computing the sum of the weights of the edges in that spanning tree. 

- A minimum spanning tree (MST) or minimum weight spanning tree is then a spanning tree with weight less than or equal to the weight of every other spanning tree.

- One example would be a cable TV company laying cable to a new neighbourhood. If it is constrained to bury the cable only along certain paths, then there would be a graph representing which points are connected by those paths.

- Some of those paths might be more expensive, because they are longer, or require the cable to be buried deeper; these paths would be represented by edges with larger weights. 

- A spanning tree for that graph would be a subset of those paths that has no cycles but still connects to every house. 

- There might be several spanning trees possible. A minimum spanning tree would be one with the lowest total cost.


### <mark style="background: #BD6500;">Example:</mark>

- ![](https://i.imgur.com/89ioPqt.png)
- This figure shows there may be more than one minimum spanning tree in a graph. In the figure, the two trees below the graph are two possibilities of minimum spanning tree of the given graph.

# <mark style="background: #BD6500;">06. Prim's Algorithm</mark>


### <mark style="background: #BD6500;">Prim's MST Algorithm:</mark>

- In computer science, Prim's algorithm is a greedy algorithm that finds a minimum spanning tree for a connected weighted undirected graph. 

- This means it finds a subset of the edges that forms a tree that includes every vertex, where the total weight of all the edges in the tree is minimized. 

- The algorithm was developed in 1930 by Czech mathematician Vojtěch Jarník and later independently by computer scientist Robert C. Prim in 1957 and rediscovered by Edsger Dijkstra in 1959. Therefore it is also sometimes called the DJP algorithm, the Jarník algorithm, or the Prim–Jarník algorithm.

- The algorithm continuously increases the size of a tree, one edge at a time, starting with a tree consisting of a single vertex, until it spans all vertices.
	- <mark style="background: #BD6500;">Input:</mark> A non-empty connected weighted graph with vertices V and edges E.
	- <mark style="background: #BD6500;">Initialise:</mark> V<sub>new</sub> = {x}, where x is an arbitrary node (starting point) from V, E<sub>new</sub> = {}
	- <mark style="background: #BD6500;">Repeat</mark> until V<sub>new</sub> = V:
	- Choose an edge (u, v) with minimal weight such that u is in V<sub>new</sub> and v is not (if there are multiple edges with the same weight, any of them may be picked)
	- Add v to V<sub>new</sub>, and (u, v) to E<sub>new</sub>
	- <mark style="background: #BD6500;">Output:</mark> V<sub>new</sub> and E<sub>new</sub> describe a minimal spanning tree

Validity of this algorithm is based on the property (which can be proved):

 <mark style="background: #BD6500;">MST Property:</mark>

- Given any division of the vertices of a graph into two sets, the shortest edge which connects a vertex in one of the sets to a vertex in the other set is part of a MST.

### <mark style="background: #BD6500;">Example 1:</mark>

- ![](https://i.imgur.com/AjyEF4k.png)

- Heap, distance[] and parent[] array updates can be seen from what follows.
- ![](https://i.imgur.com/VwATqhx.png)

### <mark style="background: #BD6500;">Example 2 - Shows more algorithm detail:</mark>

- ![](https://i.imgur.com/y1vGNcO.png)

- ![](https://i.imgur.com/DBJV14V.png)

- ![](https://i.imgur.com/PAdHNUY.png)

- ![](https://i.imgur.com/vSX0fLL.png)

- Initial state of parent and distance arrays:
- ![](https://i.imgur.com/XbUkPTn.png)

- Changes to distance and parent arrays as algorithm progresses
- ![](https://i.imgur.com/162gjbx.png)
- ![](https://i.imgur.com/5DQ0Dxm.png)
### <mark style="background: #BD6500;">Data Structures Required for Adjacency Lists representation
</mark>

- a Java/C#/C++ class called ``GraphLists`` to encapsulate most of the data structures and methods
- a Node structure for lined lists. Use these to store graph edges in the linked lists
- array of linked lists to store the graph in memory. Declared with 
```Java
Node[] adj; 
(Node ** adj; //in C++)
```
- an int array ``dist[ ]`` to record the current distance of a vertex from the MST.
- an int array ``parent[ ]`` to store the MST
- a heap h to find the next vertex nearest the MST so that it can be added to the MST. The heap minimises the number of steps in finding the next nearest vertex. log V steps instead of V steps in sequential search.
- an int array ``hPos[ ]`` which records the position of any vertex with the heap array ``a[ ]``. So vertex v is in position ``hPos[v]`` in ``a[]``.
 
<mark style="background: #BD6500;">Prim's MST Algorithm on Adjacency Lists:</mark>

```Java
Prim_Lists( Vertex s )
Begin
	// G = (V, E)
	foreach v ∈ V
		dist[v] := ∞
		parent[v] := 0 // treat 0 as a special null vertex
		hPos[v] := 0 // indicates that v  heap
	h = new Heap(|V|, hPos, dist) // priority queue (heap) initially empty
	h.insert(s) // s will be the root of the MST
	while (not h.isEmpty() ) // should repeat |V|-1 times
		v := h.remove() // add v to the MST
		dist[v] := -dist[v] // marks v as now in the MST
		foreach u  adj(v) // examine each neighbour u of v
			if wgt(v, u) < dist[u]
				dist[u] := wgt(v, u)
				parent[u] := v
				if u ∉ h
					h.insert( u)
				else
					h.siftUp( hPos[u])
			end if
		end for
	end while
	return parent
End
```

### <mark style="background: #BD6500;">Implementation Comments:</mark>

- First of all, a simple way to represent the vertices is to number them as 1, 2, 3 ... |V|.
- The most efficient way to represent the graph is to use and adjacency list, especially for sparse graphs. This is an array of linked lists. For dense ones an adjacency matrix would be fine.
- Also, a number of other data structures are used here
- The distance from a vertex u, outside of the current spanning tree, to some nearest vertex in the tree can be implemented as an array ``dist[u]``. Initially all nodes are assumed to be an infinite distance away, ∞ (or INT_MAX in C++ or int.MaxValue in C# ).
- An array ``parent[u]`` keeps track of the parent vertex of u in the MST as it grows. In fact parent[ ] stores the MST.
- The heap vertex with the highest priority is the one closest to the MST being built, i.e. the vertex u where ``dist[u]`` is a minimum. This suggests a priority queue or heap to store vertices which are outside the current MST and are being considered for inclusion.
- When vertex u is stored on the heap, only the number that represents it is stored on the heap. Its priority is stored separately This cannot be used for positioning it within the heap. Instead use ``dist[u]`` to store its priority.
- Nodes will be positioned within the heap according to their distance from the MSP being built. So the heap data structure will need a pointer to ``dist[ ]``. Then instead of have something like ``v > a[k/2]``, one would have ``dist[v] < dist[a[k/2]]``.
- If a is the heap array, then ``a[i]`` given the vertex at position i in the heap, i.e. ``a[]`` maps from a heap position or index to a vertex.
- When ``siftUp()`` is performed on a node u in the heap, its position in the heap will be required.
- We need to map from a vertex to a heap position, which is the opposite of what a[] does. Use a<sup>-1</sup> for this. Both a and a<sup>-1</sup> are be implemented as arrays. Call a<sup>-1</sup>() hPos[] if you want.

```
a : Index -> Vertex
hPos : Vertex -> Index
```

- ``siftUp()`` and ``siftDown()`` should take are of adjusting ``hPos[]``;
- On finding a shorter edge connecting a vertex u to the MST being built, its priority within the heap increases and so ``siftUp()`` would be called as in:
- ``siftUp( hPos [u])``
- The heap will need to update both ``a[]`` and ``hPos[]`` and will need access to ``dist[]``.
- A good way to give the heap access to the ``dist[]`` and ``hPos[]`` arrays is to pass them as parameter arguments to the heap constructor.
- In the main method could have
```Java
Graph g = new Graph(fileName);
mst = g.Prim( 3);
```

### <mark style="background: #BD6500;">Example 3</mark>

- ![](https://i.imgur.com/AgyAWVZ.png)
- ![](https://i.imgur.com/uCKBfCo.png)

### <mark style="background: #BD6500;">Prim's Algorithm on an Adjacency Matrix</mark>

```Java

Prim_Matrix ( Vertex s )
	// G = (V, E)
	foreach v ∈ V
		dist[v] := ∞
		parent[v] := null
	v := s // s will be the root of the MSP
	dist[null] := ∞
	
	while v != null // should repeat |V|-1 times 
		dist[v] := -dist[v] // marks v as now in the MST
		min := null
		
		foreach u from 1 to |V| // examine matrix row
			if u  adj(v)  wgt(v, u) < dist[u]
				dist[u] := wgt(v, u)
				parent[u] := v
			
			if dist[u] < dist[min] ^ dist(u) > 0
				min := u
			
			v := min
		end while
	return parent
End
```

### <mark style="background: #BD6500;">Time Complexity Analysis:</mark>

- Time Complexity Analysis Adjacency Lists Graph with Heap
- Heap contains up to V vertices. So a heap operation requires a maximum of log<sub>2</sub>*V* steps.
- Initialisation <mark style="background: #BD6500;">for loop</mark> – requires V steps

<mark style="background: #BD6500;">while loop</mark>
- each vertex is removed from heap once – so requires at most *V*log<sub>2</sub>*V* steps
- foreach loop within the while loop causes all the linked list nodes of the graph representation to be iterated thru once and since each list node represents an edge, the total number of iterations is E
- so each edge is examined once and may involve an ``insert()`` or a ``siftUp()`` . In total this means at most *E*log<sub>2</sub>*V* steps.
- Therefore complexity = O(*V* + *V* log<sub>2</sub>*V* + *E*log<sub>2</sub>*V*) ≈ O(*E*log<sub>2</sub>*V*)
- For a <mark style="background: #BD6500;">sparse</mark> graph <mark style="background: #BD6500;">E ≈ kV</mark> (k some constant), so complexity ≈ O(*E*log<sub>2</sub>V) = O(*V*log<sub>2</sub>*V*)
- For a <mark style="background: #BD6500;">dense</mark> graph <mark style="background: #BD6500;">E ≈ V<sup>2</sup></mark>, so complexity ≈ O(*E*log<sub>2</sub>V) = O(*V*<sup>2</sup>log<sub>2</sub>*V*)

### <mark style="background: #BD6500;">Adjacency Matrix Graph:</mark>

In this representation no heap is used and the while loop + for loop combination iterates through the whole matrix, i.e. V<sup>2</sup> steps. So for both sparse and dense graphs in matrix representation:

Complexity = O(V<sup>2</sup>)

| Minimum edge weight data structure                                     | Time complexity (total) |
| ---------------------------------------------------------------------- | ----------------------- |
| adjacency matrix for dense or sparse graph                             | O(V<sup>2</sup>)        |
| binary heap and adjacency lists for sparse<br>graph                    | O(V log V)              |
| binary heap and adjacency lists for dense<br>graph (E ≈ V<sup>2</sup>) | O(V<sup>2</sup> log V)  |
| Fibonacci heap and adjacency list                                      | O( E + V log V )        |

Since V<sup>2</sup> >> V log<sub>2</sub>V as V get larger, one would expect adjacency list performance to be much faster on sparse graphs.

Furthermore, adjacency lists use only the required memory for sparse graphs and are more efficient space-wise for sparse graphs. Matrix representation is very inefficient both memory wise and in performance for sparse graphs.

Better to use an adjacency matrix for a dense graph, in which case which gives complexity O(V<sup>2</sup>) and adjacency lists for sparse graphs  O(V<sub>2</sub> log V)

# <mark style="background: #BD6500;">07. Dijkstra's Shortest Path Tree Algorithm</mark>


- This algorithm is nearly identical to one for finding the minimum spanning tree.
- Both use Priority or Best First Search for Vertices Approach
- ![](https://i.imgur.com/hbONkFy.png)
- On running the algorithm for this graph and inserting output code into the algorithm, the following output was obtained:
- ![](https://i.imgur.com/mqwOiud.png)

<mark style="background: #BD6500;">Pseudocode:</mark>

```Java
Graph::SPT_Dijkstra(vertex s)
Begin
	// G = (V, E)
	for each v ∈ V
		dist[v] = ∞
		parent[v] = null // have a special null vertex
		hpos[v] = 0 // indicates that v ∉ heap
	pq = new Heap // priority queue (heap) initially empty
	v = s // s will be the root of the shortest path tree
	dist[s] = 0
		
	while v ≠ null // Loop should repeat |V|-1 times
		for each u ∈ adj(v) // Examine each neighbour u of v
			d = wgt(v,u)
			if dist[v] + d < dist[u]
				dist[u] = dist[v] + d // After changing dist[u] either insert
				if u ∉ pq // it or sift it up in the heap and record
					pq.insert( u) // its new parent vertex.
				else
					pq.siftUp( hpos[u])
					parent[u] = v
			end if
		end for
		
		v = pq.remove()
	while end
	return parent
End
```

### <mark style="background: #BD6500;">Complexity:</mark>

- Heap contains vertices. So a heap operation requires a maximum of log<sub>2</sub>*V* steps.
- Initialisation for loop – requires *V* steps
- Each node bar the first is inserted into heap once - requires at most *V*log<sub>2</sub>*V* steps
- Each edge is examined once and may modify a vertex’s position on the heap , a ``siftUp()`` which requires at most *E*log<sub>2</sub>*V*

- Therefore complexity = O(*V* + *V* log<sub>2</sub>*V* + *E*log<sub>2</sub>*V* ) ≈ O((*V* + *E*)log<sub>2</sub>*V* )

- For a <mark style="background: #BD6500;">sparse</mark> graph E ≈ kV (k some constant), so complexity ≈ O((*V* + *kV* )log<sub>2</sub>V ) = O(*V* log<sub>2</sub>*V*)

- For a <mark style="background: #BD6500;">dense</mark> graph E ≈ *V2*, so complexity ≈ O((*V*+*V*<sup>2</sup>)log<sub>2</sub>*V* ) = O(V<sup>2</sup>log<sub>2</sub>V)

### <mark style="background: #BD6500;">Data Structures Required</mark>

- a C++ class called <mark style="background: #BD6500;">Graph</mark> to encapsulate most of the data structures and methods.
- a Node structure. Use these to store graph edges in the linked lists.
- array of linked lists to store the graph in memory. Declared with ``Node ** adj;``
- an int array ``dist[ ]`` to record the current distance of a graph vertex from the starting vertex ``s``.
- an int array ``parent[ ]`` to store the SPT.
- a priority queue or heap ``pq`` to find the next vertex nearest s so that it can be added to the SPT. ``pq`` will contain an internal heap array ``h[ ]``.
- an int array ``hPos[ ]`` which records the position of any vertex with the heap array ``h[ ]``. So vertex ``v`` is in position ``hPos[v]`` in ``h[]``.

### <mark style="background: #BD6500;">Implementation Comments:</mark>

- See notes on MST algorithm. Both algorithms are very similar.
- A possible class declaration is:

```Java
class AdjGraph 
{
	private:
		struct Node 
		{
			int vert;
			int wgt;
			Node * next;
		};
		int V, E;
		Node * z;
		Node **adj;
		
	public:
	AdjGraph();
	AdjGraph(char filename[]);
	int * SPT_Dijkstra( int s);
};
```

- In the main method could have
```Java
AdjGraph g;
spt = g.SPT_Dijkstra( 1);
```

# <mark style="background: #BD6500;">08. Union-Find Data Structure</mark>

- In computer science, a union–find data structure, also called a disjoint-set data structure or merge–find set, is a data structure that keeps track of a set of elements partitioned into a number of disjoint (nonoverlapping) subsets. It supports two useful operations:

- <mark style="background: #BD6500;">findSet():</mark> Determine which subset a particular element is in. ``findSet()`` typically returns an item from this set that serves as its "representative"; by comparing the result of two ``findSet()`` operations, one can determine whether two elements are in the same subset.

- <mark style="background: #BD6500;">union():</mark> Join two subsets into a single subset.

- The other important operation, <mark style="background: #BD6500;">makeSet()</mark>, which makes a set containing only a given element (a singleton), is generally trivial. With these three operations, many practical partitioning problems can be solved.

- In order to define these operations more precisely, some way of representing the sets is needed. One common approach is to select a fixed element of each set, called its representative, to represent the set as a whole. Then, ``findSet(x)`` returns the representative of the set that x belongs to, and union takes two set representatives as its arguments.

- Two standard implementations are: <mark style="background: #BD6500;">Union-find linked lists</mark> and <mark style="background: #BD6500;">Union-find forest</mark>. In linked list method, ``findSet()`` requires 1 step, whereas ``union()`` requires many steps. The opposite is holds for union-find forest method.

### <mark style="background: #BD6500;">Union-find forest</mark>

- In this approach each set is represented by a tree data structure. When trees are used to represent the disjoint union-find sets, the tree root is used to label the set. 

- All the vertices on a tree are considered to be in the same set. In some applications, initially each vertex is in a singleton set and is the root of its own tree. 

- In general a set a tree node points to its parent on the tree and the root node points to itself. This allow a traversal from a set element to the tree root in a simple manner.

- A simple array ``parent[V+1]`` is sufficient for this where ``parent[u]`` indicates the vertex that u is attached to in the tree. Note that: ``parent[root] == root``.

- In this approach, ``findSet(u)`` means travelling back the tree from vertex u until the root is found and so may take more than 1 step. These operations are illustrated below in example below.

### <mark style="background: #BD6500;">Union-find Example</mark>

- I will use trees to represent the sets and these trees can be stored in a simple 1-D array
- Consider the sets {A, B, D, G}, {C, E, F} {H}

- Could be stored as:
- ![](https://i.imgur.com/HzoeIT4.png)

- Each set is identified by the root of its tree
- So ``findSet(G) = A`` and ``findSet(F) = C``

- ![](https://i.imgur.com/xq1SSfi.png)
- ``A != C``, so ``G`` and ``F`` are in two different sets
- union(set<sub>G</sub>, set<sub>F</sub>,) = union(A, C) gives:
- ![](https://i.imgur.com/6gQHqJk.png)
- ![](https://i.imgur.com/kqGIuFh.png)

### <mark style="background: #BD6500;">Pseudocode:</mark>

```Java
function makeSet(x)
	treeParent[x] := x
	
function findSet(x)
	if treeParent[x] == x
		return x
	else
		return findSet(treeParent[x])
	
function union(xRoot, yRoot)
	treeParent[yRoot] := xRoot
```

### <mark style="background: #BD6500;">Improvements:</mark>

<mark style="background: #BD6500;">Union by rank:</mark>

- The first way, called union by rank, is to always attach the smaller tree to the root of the larger tree.
- Since it is the depth of the tree that affects the running time, the tree with smaller depth gets added under the root of the deeper tree, which only increases the depth if the depths were equal.  
- In the context of this algorithm, the term rank is used instead of depth since it stops being equal to the depth if path compression (described below) is also used. One-element trees are defined to have a rank of zero, and whenever two trees of the same rank r are united, the rank of the result is r+1. 
- Just applying this technique alone yields a worst-case running-time of O(log n) for the Union or Find operation.

<mark style="background: #BD6500;">Path compression:</mark>

- The second improvement, called path compression, is a way of flattening the structure of the tree whenever ``findSet()`` is used on it. The idea is that each node visited on the way to a root node may as well be attached directly to the root node; they all share the same representative. 
- To effect this, as ``findSet()`` recursively traverses up the tree, it changes each node's parent reference to point to the root that it found. The resulting tree is much flatter, speeding up future operations not only on these elements but on those referencing them.

### <mark style="background: #BD6500;">Pseudocode:</mark>

```Java
function makeSet(x)
	parent[x] := x
	rank[x] := 0

function Union(xRoot, yRoot)
	// x and y are not already in same set. Merge them.
	if rank[xRoot] < rank[yRoot]
		parent[xRoot] := yRoot
	else if rank[xRoot] > rank[yRoot]
		parent[yRoot] := xRoot
	else
		parent[yRoot] := xRoot
		rank[xRoot] := rank[xRoot] + 1

function findSet(x)
	if parent[x] != x
		parent[x] := findSet(parent[x])
	return parent[x]
```

# <mark style="background: #BD6500;">09. Kruskal's MST Algorithm</mark>

- Kruskal's algorithm is an algorithm in graph theory that finds a minimum spanning tree for a connected weighted graph. 
- This means it finds a subset of the edges that forms a tree that includes every vertex, where the total weight of all the edges in the tree is minimized. If the graph is not connected, then it finds a minimum spanning forest (a minimum spanning tree for each connected component). 
- Kruskal's algorithm is an example of a greedy algorithm

### <mark style="background: #BD6500;">Description:</mark>

- Create a forest *T* (a set of trees), where each vertex in the graph is a separate tree
- Create a set *S* containing all the edges in the graph
- While *S* is non-empty and *T* is not yet spanning
	- remove an edge with minimum weight from *S*
	- if that edge connects two different trees, then add it to the forest, combining two trees into a single tree, otherwise discard that edge.
	
- At the termination of the algorithm, the forest has only one component and forms a minimum spanning tree of the graph.

### <mark style="background: #BD6500;">Alternate Description (Pseudocode):</mark>

```Java
KRUSKAL(G):
T = ∅
foreach v ∈ G.V:
	MAKE-SET(v)

foreach (u, v) ordered by weight(u, v), increasing:
	if FIND-SET(u) ≠ FIND-SET(v):
	T = T ∪ {(u, v)}
	UNION(u, v)
	return T
```

### <mark style="background: #BD6500;">Data Structure Consideration</mark>

- To implement this algorithm a way to represent sets, to find which set a vertex is in and to get the union of two sets is required. 
- We refer to a data structure which supports this as a Union-Find data structure. For junior undergraduates, it may seem difficult to implement. Two standard implementations are available: <mark style="background: #BD6500;">Disjoint-set linked lists</mark> and <mark style="background: #BD6500;">Disjoint-set trees</mark>.

### <mark style="background: #BD6500;">Example 1:</mark>

- Initially all 11 edges are in the heap and each vertex is isolated. Then after next 2 minimum edges A-5-D and C-5-E are chosen as shown.
- ![](https://i.imgur.com/m1NWZyX.png)

- MST trees are { {A} {B} {C} {D} {E} {F} {G}}.

- Then D-6-F and B-7-E chosen.

- ![](https://i.imgur.com/VtDEpgq.png)


- Next A-7-B is chosen which joins 2 trees. 
- ![](https://i.imgur.com/wxw4GNu.png)

- But next 3 edges chosen are B-8-C, E-8-F and D-9-B which would give rise to cycles, and so are ignored.
- ![](https://i.imgur.com/VSnRhKG.png)

- Edge E-9-G completes the MST, the algorithm stops here as all vertices are now in the MST. Note there are still 2 edges left, F-11-G and D-15-E, but they don’t matter.

- ![](https://i.imgur.com/xw47Ukl.png)

### <mark style="background: #BD6500;">Union-find Trees Representation</mark>

- When trees are used to represent the disjoint union-find sets each set is represented by a tree and the tree root is used to label the set. All the vertices on a tree are considered to be in the same set. 
- Initially each vertex is in a singleton set and is the root of its own tree. In general a vertex points to its parent on the tree and the root vertex points to itself. #
- This allow a traversal from a vertex to the tree root in a simple manner. A simple array ``parent[V+1]`` is sufficient for this where ``parent[u]`` indicates the vertex that ``u`` is attached to in the tree. Note ``parent[root] == root``. 
- In this approach, ``find(u)`` means travelling back the tree from vertex u until the root is found and so may take more than 1 step. Once the two roots ``Cu`` and ``Cv`` are found, the ``union(Cu , Cv)`` takes 1 step and just involves linking one root to the other. These operations are illustrated below.
- ![](https://i.imgur.com/z2nE8bh.png)

### <mark style="background: #BD6500;">Algorithm in Pseudocode</mark>

```Java
MST_Kruskal()
begin
	// Input is simple connected graph represented by array of edges edge[]
	// Output is list of edges T in MST
	// Create a partition for the set of vertices
	foreach vertex v  V
		Cv := {v}
	
	// create a minHeap h from array of edges E
	h := new Heap( E)
	
	// let T be an initially empty tree
	T := ∅
	while size(T) < n-1
		(u, v, wgt) := h.removeMin()
		Cv := findSet(v)
		Cu := findSet(u)
		
	if Cu  Cv
		union(Cu , Cv)
		T := T ∪ {(u, v, wgt)}
	return T
end
```

### <mark style="background: #BD6500;">Time Complexity</mark>

- Kruskal's algorithm can be shown to run in O(*E* log V) time. 
- By way of comparison Prim complexity is O( *E* log V ) for sparse and O(V<sup>2</sup>) = O(E) for dense.

- So for sparse graphs the performance is similar and for dense graphs Prim on an adjacency matrix is better.

### <mark style="background: #BD6500;">Implementation Concerns</mark>

- A union-find data structure is required for Kruskal’s algorithm. At any stage of the algorithm, the graph vertices are partitioned into disjoint sets. When an edge is being considered for the MST, we must first find which sets the edge vertices belong to. Hence a <mark style="background: #BD6500;">findSet()</mark> operation is required. If the vertex sets are disjoint, the edge is added to the MST and the union of the two sets is obtained.

- So a <mark style="background: #BD6500;">union()</mark> operation is also needed.
	- <mark style="background: #BD6500;">findSet:</mark> Vertex -> Set
	- <mark style="background: #BD6500;">union:</mark> Set×Set -> Set
	
- Two effective ways to implement the union-find data structure are:
	- Disjoint-set linked lists
	- Disjoint-set trees.
	
- The disjoint-set trees method when improved with union by <mark style="background: #BD6500;">rank</mark> and <mark style="background: #BD6500;">path compression</mark> offers the most efficient approach.
 
### <mark style="background: #BD6500;">Example 2 - Shows more Algorithm Detail:</mark>

- ![](https://i.imgur.com/236Oy9E.png)
- Initially connected components are just singleton sets with individual vertices:
	- {A} {B} {C} {D} {E} {F} {G} {H} {I} {J} {K} {L} {M}

- After the following five minimum edges
	- A-1-B
	- D-1-F
	- E-1-G
	- J-1-K,
	- L-1-M
- have been added to the MST, components are:
- {A,B} {D,F} {C} {E,G} {H} {I} {J,K} {L,M}

- ![](https://i.imgur.com/83hrh9h.png)
- Choosing 3 more minimum edges of weight 1,
	- B-1-C
	- G-1-J
	- K-1-I

- we will have five connected components:
	- {A,B,C} {D,F} {E,G,J,K,I} {H} {L,M}
	
- ![](https://i.imgur.com/wqiyafE.png)

- Next supposing the following minimum edges are chosen:
	- A-2-F
	- {A,B,C,D,F} {E,G,J,K,I} {H} {L,M}
	- H-2-I
	- {A,B,C,D,F} {E,G,J,K,I,H} {L,M}
	- J-2-M
	- {A,B,C,D,F} {E,G,J,K,I,H,L,M}
	- And finally add edge D-2-E to get one connected component::
	- {A,B,C,D,F,E,G,J,K,I,H,L,M}
	
- ![](https://i.imgur.com/5bvPKDm.png)


# <mark style="background: #BD6500;">10. Quick Sort</mark>

- Quick sort was discovered by Tony Hoare in 1960. In general it has much better performance than brute force sorting methods like bubble sort or selection sort - O(n log<sub>2</sub> n) versus O(n<sup>2</sup>) . It works by first of all by partitioning the array around a pivot value and then dealing with the 2 smaller partitions separately.

- Partitioning is the most complex part of quick sort. The simplest thing is to use the first value in the array, ``a[l]`` (or ``a[0]`` as ``l = 0`` to begin with) as the pivot. 

- After the partitioning, all values to the left of the pivot are <= pivot and all values to the right are > pivot.

- For example, consider:
- ![](https://i.imgur.com/sVIRsDm.png)

- where the value of ``a[l]``, namely 8, is chosen as pivot. Then the partition function moves along the array from the lhs until it finds a value > pivot. Next it moves from the rhs, passing values > pivot and stops when it finds a value <= pivot. This is done by the following piece of code:
```Java
i = l; j = r+1;

do ++i;
while( a[i] <= pivot && i <= r );

do --j;
while( a[j] > pivot );
```

- Then if the lhs value is to the left of the rhs value, they are swapped. Variable ``i`` keeps track of the current position on moving from left to right and j does the same for moving from right to left. You then get
- ![](https://i.imgur.com/ZCY9n8U.png)

- ``a[i]`` and ``a[j]`` are swapped to give
- ![](https://i.imgur.com/mT4ku3z.png)

- This process is repeated with ``i`` and ``j`` to get

- ![](https://i.imgur.com/TBpY4Mv.png)

- and do a swap to get
- ![](https://i.imgur.com/exkuczS.png)

- Move ``i`` and ``j`` again to get
- ![](https://i.imgur.com/ktRW9Ba.png)
- and swap again
- ![](https://i.imgur.com/Wi1660u.png)

- Move ``i`` and ``j`` again.
- ![](https://i.imgur.com/Ob8G29l.png)

- When j passes i, the partitioning is finished. At this stage the partition code breaks out of the main while loop.
- All ``a[k]`` <= pivot where k <= j. All that we do next is swap the pivot with ``a[j]`` to get
- ![](https://i.imgur.com/D4h7VWv.png)

- Then quickSort is called again separately on the two smaller arrays (here ``a[0]`` to ``a[5]`` and ``a[7]`` to ``a[12]``). The pivot is left alone as it is in the correct position. So quickSort divides the problem into two smaller ones and recursively calls itself on each of then as in:
```Java
quickSort( a, l, j-1) or quickSort( a, 0, 5)
quickSort( a, j+1, r) or quickSort( a, 7, 12)
```

- The smaller arrays are again partitioned in the same way as described above and so on. Eventually quickSort will arrive at arrays of size 1 or 2 or 0. Arrays of size 0 or 1 are already so to say sorted, while an array of size 2 can be sorted with an if statement. 
- It is a waste of computation power to partition an array of size 2 and call quickSort twice more. The lhs array is similarly partitioned from
- ![](https://i.imgur.com/pISOJPP.png)

- Next do
```Java
quickSort( a, 0, 3)
quickSort( a, 5, 5) – no more partition in rhs subarray.
```

- Next ``quickSort( a, 0, 3)`` is tackled which partitions subarray as follows:
- ![](https://i.imgur.com/nm6X1M8.png)

- Next do
```Java
quickSort( a, 0, 1)
quickSort( a, 3, 3) – no more partition in rhs subarray.
```

- The lhs subarray is again partitioned and a swap done
- ![](https://i.imgur.com/xbidHbs.png)

- Next do
```Java
quickSort( a, 0, 0) – no more partition in lhs subarray.
```

- Next we return to the original lhs subarray from the first partition
```Java
quickSort( a, 7, 12)
```

- which partitions subarray as follows:
- ![](https://i.imgur.com/cwLcCnL.png)

- and calls ``quickSort( a, 7, 9)`` and ``quickSort( a, 11, 12)``.
- Next ``quickSort( a, 7, 9)`` is tackled which partitions subarray as follows:
- ![](https://i.imgur.com/XtZ3wGI.png)

- All the partitioning in now over with the result that in the meantime the array has been sorted.

<mark style="background: #BD6500;">Number of computations:</mark>
- Comparisons = 40 
- swaps = 13

### <mark style="background: #BD6500;">Overview</mark>

- ![](https://i.imgur.com/bEHn97Y.png)


- <mark style="background: #BD6500;">Note:</mark> Quick sort works its way down through partitions, creating smaller ones all the time before it deals with all partitions on a given level. This is referred to as a depth-first approach.

### <mark style="background: #BD6500;">quickSort.c</mark>

```C++
// quickSort.cpp

#include <stdio.h>
void quickSort( int[], int, int);
int partition( int[], int, int);

void main()
{
	int a[] = { 7, 12, 1, -2, 0, 15, 4, 11, 9};
	int i;
	
	printf("\n\nUnsorted array is: ");
	
	for(i = 0; i < 9; ++i)
		printf(" %d ", a[i]);
		
	quickSort( a, 0, 8);
		
	printf("\n\nSorted array is: ");
		
	for(i = 0; i < 9; ++i)
		printf(" %d ", a[i]);
}

void quickSort( int a[], int l, int r)
{
	int j;
	if( l < r )
	{
		// divide and conquer
		j = partition( a, l, r);
		quickSort( a, l, j-1);
		quickSort( a, j+1, r);
	}
}

int partition( int a[], int l, int r) 
{
	int pivot, i, j, temp;
	pivot = a[l];
	i = l; j = r+1;
	
	while( 1)
	{
		do ++i; while( a[i] <= pivot && i <= r );
		do --j; while( a[j] > pivot );
		
		if( i >= j ) break;
			temp = a[i]; a[i] = a[j]); a[j] = temp;
			
	}
	
	temp = a[l]; a[l] = a[j]); a[j] = temp;
	return j;
}
```

### <mark style="background: #BD6500;">Version from Sedgewick </mark>

```C++
// quickSort_Sedgew.cpp
#include <stdio.h>

void quickSort( int[], int, int);

void main()
{
	int a[] = { 7, 12, 1, -2, 0, 15, 4, 11, 9};
	int i;
	
	printf("\n\nUnsorted array is: ");
	
	for(i = 0; i < 9; ++i)
		printf(" %d ", a[i]);
	
	quickSort( a, 0, 8);
	printf("\n\nSorted array is: ");
	
	for(i = 0; i < 9; ++i)
		printf(" %d ", a[i]);
}

void quickSort( int a[], int l, int r)
{
	int pivot, i, j, t;
	
	if( l < r )
	{
		pivot = a[l];
		i = l; j = r+1;
		
		while( 1)
		{
			do ++i; while( a[i] <= pivot && i <= r );
			do --j; while( a[j] > pivot );
			
			if( i >= j ) 
				break;
			
			t = a[i]; 
			a[i] = a[j]; 
			a[j] = t;
			
		}
		
		t = a[l]; a[l] = a[j]; a[j] = t;
		
		quickSort( a, l, j-1);
		quickSort( a, j+1, r);
	}
}
```

### <mark style="background: #BD6500;">Quick Sort version 2</mark>

- This version is more efficient when dealing with small subarrays.

```C++
// quickSort_Ver2.cpp
// more efficient near end of sorting
// main() etc left out

void quickSort( int a[], int l, int r)
{
	int pivot, i, j, t;
	// sub array of size 1 or 0 - already sorted
	if(l >= r )
		return;
	// array of size 2, sort directly with if
	
	if( l+1 == r) 
	{
		if(a[l] > a[r]) 
		{
			t = a[l]; a[l] = a[r]; a[r] = t;
		}
		return;
	}
	
	pivot = a[l];
	i = l; j = r+1;
	
	while( 1)
	{
		do ++i; while( a[i] <= pivot && i <= r );
		do --j; while( a[j] > pivot );
		
		if( i >= j ) 
			break;
		
		t = a[i]; 
		a[i] = a[j]; 
		a[j] = t;
	}
	t = a[l]; a[l] = a[j]; a[j] = t;
	quickSort( a, l, j-1);
	quickSort( a, j+1, r);
}
```

# <mark style="background: #BD6500;">11. Heap Sort</mark>

- You may have noticed that in a max heap, the largest value can easily be removed from the top of the heap and in the ensuing ``siftDown()`` a 'free' slot is made available at what was the end of the heap.
- The removed value could then be stored in the vacated slot. If this process was repeated until the heap shrank to size 1, we would have a sorted array.
- This suggests the basis of a new sorting algorithm, namely Heap Sort.
- For sorting general purpose arrays, a heap going from array positions 0 to (n-1) is more appropriate than what we used in our Heap class. In this situation:
- ``parent(i) = (i-1)/2, lchild(i) = 2i+1, rchild(i) = 2i+2``

- But first of all it is necessary to convert the array into a heap array. We can do this in two ways:
1. A top-down approach whereby we insert array values one at a time into a heap initially consisting of the first array value. This approach can be summarised with:

```Java
for k = 2 to (n-1) // array of size n, a[0] to a[n-1]
	siftUp(k, a)
```

2. A bottom up approach can also be used to do this whereby 2 smaller heaps and a value are combined to give a bigger heap. Consider the diagram below, which shows two small heaps h1 and h2 and a value x. Because y is the biggest value in h1 and z is the biggest in h2, we can simply merge h1, h2 and x into a new heap by a ``siftDown()`` starting at x's position.

- ![](https://i.imgur.com/blNVHGP.png)

- The smallest heaps are of size 1 and are the leaf nodes of the binary tree. The last tree node with a leaf node for a left child is at position (n-1)/2 where n is the array size. So by iterating the above described procedure starting from the node at (n-1)/2, we gradually construct a heap. It can be shown that constructing a heap in this way from an array takes *n* steps where *n* is the array size.

- This process can be expressed as:

```Java
for k = (n-1-1)/2 to 0
	siftDown(k, a, n)
```

- It can be shown that constructing a heap in this way from an array takes n steps where *n* is the array size. Loop complexity is O(*n*). For this reason we use this approach.

### <mark style="background: #BD6500;">Example:</mark>

- For example, consider the array below which is also shown as a binary tree. Here ``n = 8``. The last node with a child is the one containing 9 at position (8-1)/2 = 3.
- The next node to be sifted down is at position 2. It has the value 1. Then positions 1 and 0 are processed.
- ![](https://i.imgur.com/Xu7lW8p.png)

### <mark style="background: #BD6500;">Using the heap for sorting</mark>

- Now that a heap has been obtained by rearranging ``a[ ]``, we begin to sort it by removing the highest priority value from the heap and placing it at the end of the array.
- So the largest value is removed from the heap and the heap resized. This requires a ``siftDown()`` so that the smaller ‘heap’ is still a heap and this operation takes at most log<sub>2</sub>n steps. 
- The removed value is then placed at the array position which has been freed by the removal. This is repeated with the next largest value being placed in the second last position and so on. This process is repeated ``n - 1`` times.
- We express this algorithm with:

```Java
for k = n-1 to 1
	v = a[0] // largest value on heap
	a[0] = a[k] // a[k] is last value on heap
	siftDown( 0, a, k) // k is now heap size
	a[k] = v
```

### <mark style="background: #BD6500;">Example continued:</mark>

- ![](https://i.imgur.com/M4MTjLQ.png)

### <mark style="background: #BD6500;">Calculating heap sort complexity</mark>

- Heap sort requires:
	- n steps to form the heap
	- and (n - 1)log2 n steps in the siftDowns.
	
- So the total number of steps is *n* + (*n* -1)log<sub>2</sub> *n*  ≈ *n* log<sub>2</sub> *n*

- This is the same as the average cost of quick sort.
	- Complexity of heap sort = O(*n* log<sub>2</sub> *n*)

- The average and worst performance of heap sort is *n* log<sub>2</sub> *n* which is also the average performance of quick sort. However, quick sort can be unstable in its performance depending on how well it chooses a pivot. At worst quick sort takes n<sup>2</sup>/2steps. So if you are not sure about the nature of the data and want guaranteed performance, heap sort is better.

### <mark style="background: #BD6500;">Algorithm:</mark>

- Finally, the pseudocode fragments are put together to yield

```Java
// assuming position a[0] does contains data

heapSort( int a[ ], int n )
begin
	for k = n/2 - 1 to 0
		siftDown(k, a, n)
		
	for k = n-1 to 1
		v = a[0] // largest value on heap
		a[0] = a[k]
		siftDown( 0, a, k) // heap size is now k
		a[k] = v //a[k] is no longer in heap

end

// Heap from a[0] to a[N-1], size N
siftDown(int k, int a[ ], int N)
begin
	v = a[k]
	j = 2k + 1 // left child of k since heap begins in a[0]
	
	while( j ≤ N-1 ) // while left child is within heap
		if( j < N-1 ^ a[j] < a[j+1])
			++j
			
		if( v >= a[j] )
			break
			
		a[k] = a[j]
		k = j
		j = 2k+1
	a[k] = v
end
```

# <mark style="background: #BD6500;">12. Merge Sort</mark>

- This follows the divide and conquer approach in contrast to quick sort which is more akin to conquer and divide. Merge sort divides the array and does the work of recombining (conquering) the subparts afterwards whereas quick sort does the work of partitioning (conquering) first and then divides into 2 smaller quick sorts..
- ![](https://i.imgur.com/3i9ux8k.png)

### <mark style="background: #BD6500;">Pseudocode:</mark>
```Java
// a is an array of size n
mergeSort( a, n)
	int * b := new int[n]
	mSort( a, b, 0, n-1)

// a and b are arrays, l is left index, r is right index
mSort( a, b, l, r)
	if r > l
		m := (r + l) / 2
		mSort(a, b, l, m)
		mSort(a, b, m+1, r)
		// copy lhs subarray of a to b
		for i := m+1 to l+1
			b[i-1] := a[i-1]
		// copy rhs subarray of a to b in reverse order
		// b[r] := a[m+1] b[r-1] := a[m+2] ... b[m+1] := a[r]
		for j := m to r-1
			b[r+m-j] := a[j+1]
		// merge the 2 sorted subarrays in b into
		// one sorted array in a
		for k := l to r
			if b[i] < b[j]
				a[k] := b[i++ ]
			else
				a[k] := b[j--]
	```

### <mark style="background: #BD6500;">Comment on Performance:</mark>

- Merge sort always takes 2N log<sub>2</sub> N steps. On average quick sort takes N log2 N steps. You would expect merge sort to be about twice as slow due to copying to ``b[]`` and back again to ``a[]``

- However, the performance of quick sort depends on a good choice of pivot. In our approach we choose the first element as the pivot. If an array is already nearly sorted, this can lead to very poor performance for quick sort. In its worst case quick sort requires N<sup>2</sup>/2 steps which is the same performance as bubble sort and selection sort.

- The main drawbacks of merge sort as opposed to quick sort are:
	- it requires an extra auxiliary array ``b[p]``
	- on average is about twice as slow
	
- However, in situations where the data can vary in how much it is already sorted, merge sort is more stable.
- In the above pseudocode description of merge sort, copying the rhs part of ``a[]`` into ``b[]`` in reverse order makes for a slightly more efficient algorithm. Why ?

# <mark style="background: #BD6500;">13. Bubble Sort and Comb Sort</mark>

### <mark style="background: #BD6500;">Pseudocode:</mark>

```Java
bubbleSort( int a[], int n)
Begin
	for i = 1 to n-1 // n-1 repeats
		sorted := true
		for j = 0 to n-1-i
			if a[j] > a[j+1]
				temp := a[j]
				a[j] := a[j+1]
				a[j+1] := temp
				sorted := false
		end for
		
		if sorted
			break from i loop
		
	end for
End
```

- Bubble sort uses a loop (inside j loop) to travel through an array comparing adjacent values as it moves along. 
- If an array element ``a[j]`` is greater than the element immediately to its right ``a[j+1]``, it swaps them. 
- The first time around, this process will move or bubble the largest value to the end of the array. So for instance
- ![](https://i.imgur.com/dzOPrmj.png)
- will end up as
- ![](https://i.imgur.com/ToSp8Ja.png)
- This process is repeated, on the second iteration, the second largest value will be moved to the second last array position and so on. In all, the bubble process (inside j loop) is repeated n-1 times for an array of size n.

### <mark style="background: #BD6500;">Bubble Sort example:</mark>

- ![](https://i.imgur.com/dnmL5uz.png)
- Note for array of size 8, outside i loop repeats 7 times.

### <mark style="background: #BD6500;">Complexity:</mark> 

- Clearly for an array of size n, the outside loop repeats n-1 times.
- To begin with the inside loop does n-1 comparisons, next time n-2 and so on. Finally on the last iteration of the outside loop, the inside loop does 1 comparison. So on average the inside loop does ((n-1) + 1) / 2  n/2 comparisons.
- Therefore, the overall number of computation steps is n * n/2 = n<sup>2</sup>/2
- Complexity of bubble sort = O(n<sup>2</sup>)

### <mark style="background: #BD6500;">Tortoises and Hares:</mark>

- ![](https://i.imgur.com/lSKC0ZY.png)
- A tortoise is a large value on the lhs of the array, like 9 above. In one bubble pass it is bubbled to the rhs of the array. 
- In contrast, a small value referred to as a hare like 0 above on the rhs, moves only 1 step to the left on a full bubble pass. So this asymmetry is what is referred to as <mark style="background: #BD6500;">Tortoises and Hares</mark>.

### <mark style="background: #BD6500;">Comb Sort:</mark>

- The basic idea is to eliminate tortoises, or small values near the end of the list, since in a bubble sort these slow the sorting down tremendously. <mark style="background: #BD6500;">Hares</mark>, large values around the beginning of the list, do not pose a problem in bubble sort.
- In bubble sort, when any two elements are compared, they always have a gap (distance from each other) of 1. The basic idea of comb sort is that the gap can be much more than 1. The inner loop of bubble sort, which does the actual swap, is modified such that gap between swapped elements goes down (for each iteration of outer loop) in steps of a "shrink factor" k: [n/k, n/k<sup>2</sup>, n/k<sup>3</sup>, ..., 1 ].
- The gap starts out as the length of the list n being sorted divided by the shrink factor *k* (generally 1.3; see below) and one pass of the aforementioned modified bubble sort is applied with that gap.
- Then the gap is divided by the shrink factor again, the list is sorted with this new gap, and the process repeats until the gap is 1. At this point, comb sort continues using a gap of 1 until the list isfully sorted. The final stage of the sort is thus equivalent to a bubble sort, but by this time most turtles have been dealt with, so a bubble sort will be efficient.
- The shrink factor has a great effect on the efficiency of comb sort. *k* = 1.3 has been suggested as an ideal shrink factor by the authors of the original article after empirical testing on over 200,000

### <mark style="background: #BD6500;">Pseudocode:</mark>

```Java
	combSort( input[] )
	
	gap := input.size // Initialize gap size
	shrink := 1.3 // Set the gap shrink factor
	sorted := false
	
	loop while sorted = false
		// Update the gap value for a next comb
		gap := floor(gap / shrink)
		
		if gap > 1
			sorted := false // We are never sorted as long as gap > 1
		else
			gap := 1
			sorted := true // If there are no swaps this pass, we are done
		end if
		
		// A single "comb" over the input list
		i := 0
		loop while i + gap < input.size
			if input[i] > input[i+gap]
				swap(input[i], input[i+gap])
				sorted := false
				// If this assignment never happens within the loop,
				// then there have been no swaps and the list is sorted.
			end if
			
			i := i + 1
		
		end loop
	end loop
end
```

# <mark style="background: #BD6500;">14. Dictionaries</mark>

### <mark style="background: #BD6500;">Dictionary ADT</mark>

- The dictionary ADT (Abstract Data Type) models a searchable collection of key element items The main operations of a dictionary are searching, inserting, and deleting items
- Multiple items with the same key are allowed
 

<mark style="background: #BD6500;">Applications:</mark>
- address book
- credit card authorization
- mapping host names (e.g., cs16.net) to internet addresses (e.g., 128.148.34.101)

<mark style="background: #BD6500;">Dictionary ADT methods:</mark>
- <mark style="background: #BD6500;">findElement(k):</mark> if the dictionary has an item with key k, returns its element, else, returns the special element NO_SUCH_KEY
- <mark style="background: #BD6500;"> insertItem(k, o):</mark> inserts item (k, o) into the dictionary
- <mark style="background: #BD6500;">removeElement(k):</mark> if the dictionary has an item with key k, removes it from the dictionary and returns its element, else returns the special element NO_SUCH_KEY
- <mark style="background: #BD6500;">size()</mark>, <mark style="background: #BD6500;">isEmpty()</mark>
- <mark style="background: #BD6500;">keys()</mark>, <mark style="background: #BD6500;">Elements()</mark>

### <mark style="background: #BD6500;">Log File:</mark>

- A log file is a dictionary implemented by means of an unsorted sequence
- We store the items of the dictionary in a sequence (based on a doubly-linked lists or a circular array), in arbitrary order

- <mark style="background: #BD6500;">Performance:</mark>
	- <mark style="background: #BD6500;"> insertItem </mark> takes O(1) time since we can insert the new item at the beginning or at the end of the sequence
	- <mark style="background: #BD6500;">findElement</mark> and <mark style="background: #BD6500;">removeElement</mark> take O(*n*) time since in the worst case (the item is not found) we traverse the entire sequence to look for an item with the given key

- The log file is effective only for dictionaries of small size or for dictionaries on which insertions are the most common operations, while searches and removals are rarely performed (e.g., historical record of logins to a workstation)
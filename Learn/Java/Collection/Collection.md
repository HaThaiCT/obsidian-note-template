Prior to Java 2, Java provided ad hoc classes such as **Dictionary, Vector, Stack,** and **Properties** to store and manipulate groups of objects. Although these classes were quite useful, they lacked a central, unifying theme. Thus, the way that you used Vector was different from the way that you used Properties.

## Why Collections Framework?

The collections framework was designed to meet several goals, such as −

- The framework had to be high-performance. The implementations for the fundamental collections (dynamic arrays, linked lists, trees, and hashtables) were to be highly efficient.
    
- The framework had to allow different types of collections to work in a similar manner and with a high degree of interoperability.
    
- The framework had to extend and/or adapt a collection easily.
    

Towards this end, the entire collections framework is designed around a set of standard interfaces. Several standard implementations such as **LinkedList, HashSet,** and **TreeSet**, of these interfaces are provided that you may use as-is and you may also implement your own collection, if you choose.
## Java Collections Framework

A collections framework is a unified architecture for representing and manipulating collections. All collections frameworks contain the following −

- [**Interfaces**](https://www.tutorialspoint.com/java/java_interfaces.htm) − These are abstract data types that represent collections. Interfaces allow collections to be manipulated independently of the details of their representation. In [object-oriented](https://www.tutorialspoint.com/java/java_oops_concepts.htm) languages, interfaces generally form a hierarchy.
    
- **Implementations, i.e., [Classes](https://www.tutorialspoint.com/java/java_object_classes.htm)** − These are the concrete implementations of the collection interfaces. In essence, they are reusable data structures.
    
- **Algorithms** − These are the methods that perform useful computations, such as searching and sorting, on objects that implement collection interfaces. The algorithms are said to be polymorphic: that is, the same method can be used on many different implementations of the appropriate collection interface.
    

In addition to collections, the framework defines several map interfaces and classes. Maps store key/value pairs. Although maps are not _collections_ in the proper use of the term, but they are fully integrated with collections.

## Hierarchy of Collection Framework

All classes and interfaces for the collection framework are available in [java.utli package](https://www.tutorialspoint.com/java/util/index.htm). The following diagram shows the hierarchy of the collection framework in Java:

![Hierarchy of Collection Framework](https://www.tutorialspoint.com/java/images/hierarchy-of-collection-framework.jpg "Hierarchy of Collection Framework")

![Ezoic](https://go.ezodn.com/utilcave_com/ezoicbwa.png "ezoic")

## Java Collection Interfaces

The collections framework defines several interfaces. This section provides an overview of each interface −

| Sr.No. | Interface & Description                                                                                                                                                                                                                                                                     |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1      | [The Collection Interface](https://www.tutorialspoint.com/java/java_collection_interface.htm)<br><br>This enables you to work with groups of objects; it is at the top of the collections hierarchy.                                                                                        |
| 2      | [The List Interface](https://www.tutorialspoint.com/java/java_list_interface.htm)<br><br>This extends **Collection** and an instance of List stores an ordered collection of elements.                                                                                                      |
| 3      | [The Set](https://www.tutorialspoint.com/java/java_set_interface.htm)<br><br>This extends Collection to handle sets, which must contain unique elements.                                                                                                                                    |
| 4      | [The SortedSet](https://www.tutorialspoint.com/java/java_sortedset_interface.htm)<br><br>This extends Set to handle sorted sets.                                                                                                                                                            |
| 5      | [The Map](https://www.tutorialspoint.com/java/java_map_interface.htm)<br><br>This maps unique keys to values.                                                                                                                                                                               |
| 6      | [The Map.Entry](https://www.tutorialspoint.com/java/java_mapentry_interface.htm)<br><br>This describes an element (a key/value pair) in a map. This is an inner class of Map.                                                                                                               |
| 7      | [The SortedMap](https://www.tutorialspoint.com/java/java_sortedmap_interface.htm)<br><br>This extends Map so that the keys are maintained in an ascending order.                                                                                                                            |
| 8      | [The Enumeration](https://www.tutorialspoint.com/java/java_enumeration_interface.htm)<br><br>This is legacy interface defines the methods by which you can enumerate (obtain one at a time) the elements in a collection of objects. This legacy interface has been superceded by Iterator. |

## Java Collection Classes

Java provides a set of standard collection classes that implement Collection interfaces. Some of the classes provide full implementations that can be used as-is and others are abstract class, providing skeletal implementations that are used as starting points for creating concrete collections.

The standard collection classes are summarized in the following table −

| Sr.No. | Class & Description                                                                                                                                                        |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1      | **AbstractCollection**<br><br>Implements most of the Collection interface.                                                                                                 |
| 2      | **AbstractList**<br><br>Extends AbstractCollection and implements most of the List interface.                                                                              |
| 3      | **AbstractSequentialList**<br><br>Extends AbstractList for use by a collection that uses sequential rather than random access of its elements.                             |
| 4      | [LinkedList](https://www.tutorialspoint.com/java/util/java_util_linkedlist.htm)<br><br>Implements a linked list by extending AbstractSequentialList.                       |
| 5      | [ArrayList](https://www.tutorialspoint.com/java/util/java_util_arraylist.htm)<br><br>Implements a dynamic array by extending AbstractList.                                 |
| 6      | **AbstractSet**<br><br>Extends AbstractCollection and implements most of the Set interface.                                                                                |
| 7      | [HashSet](https://www.tutorialspoint.com/java/util/java_util_hashset.htm)<br><br>Extends AbstractSet for use with a hash table.                                            |
| 8      | [LinkedHashSet](https://www.tutorialspoint.com/java/util/java_util_linkedhashset.htm)<br><br>Extends HashSet to allow insertion-order iterations.                          |
| 9      | [TreeSet](https://www.tutorialspoint.com/java/util/java_util_treeset.htm)<br><br>Implements a set stored in a tree. Extends AbstractSet.                                   |
| 10     | **AbstractMap**<br><br>Implements most of the Map interface.                                                                                                               |
| 11     | [HashMap](https://www.tutorialspoint.com/java/util/java_util_hashmap.htm)<br><br>Extends AbstractMap to use a hash table.                                                  |
| 12     | [TreeMap](https://www.tutorialspoint.com/java/util/java_util_treemap.htm)<br><br>Extends AbstractMap to use a tree.                                                        |
| 13     | [WeakHashMap](https://www.tutorialspoint.com/java/util/java_util_weakhashmap.htm)<br><br>Extends AbstractMap to use a hash table with weak keys.                           |
| 14     | [LinkedHashMap](https://www.tutorialspoint.com/java/util/java_util_linkedhashmap.htm)<br><br>Extends HashMap to allow insertion-order iterations.                          |
| 15     | [IdentityHashMap](https://www.tutorialspoint.com/java/util/java_util_identityhashmap.htm)<br><br>Extends AbstractMap and uses reference equality when comparing documents. |

The _AbstractCollection, AbstractSet, AbstractList, AbstractSequentialList_ and _AbstractMap_ classes provide skeletal implementations of the core collection interfaces, to minimize the effort required to implement them.

The following legacy classes defined by java.util have been discussed in the previous chapter −

|Sr.No.|Class & Description|
|---|---|
|1|[Vector](https://www.tutorialspoint.com/java/util/java_util_vector.htm)<br><br>This implements a dynamic array. It is similar to ArrayList, but with some differences.|
|2|[Stack](https://www.tutorialspoint.com/java/util/java_util_stack.htm)<br><br>Stack is a subclass of Vector that implements a standard last-in, first-out stack.|
|3|[Dictionary](https://www.tutorialspoint.com/java/util/java_util_dictionary.htm)<br><br>Dictionary is an abstract class that represents a key/value storage repository and operates much like Map.|
|4|[Hashtable](https://www.tutorialspoint.com/java/util/java_util_hashtable.htm)<br><br>Hashtable was part of the original java.util and is a concrete implementation of a Dictionary.|
|5|[Properties](https://www.tutorialspoint.com/java/util/java_util_properties.htm)<br><br>Properties is a subclass of Hashtable. It is used to maintain lists of values in which the key is a String and the value is also a String.|
|6|[PriorityQueue](https://www.tutorialspoint.com/java/util/java_util_priorityqueue.htm)<br><br>PriorityQueue class is an unbounded priority queue based on a priority heap. A priority queue relying on natural ordering also does not permit insertion of non-comparable objects.|
|7|[BitSet](https://www.tutorialspoint.com/java/util/java_util_bitset.htm)<br><br>A BitSet class creates a special type of array that holds bit values. This array can increase in size as needed.|
|8|[ArrayDeque](https://www.tutorialspoint.com/java/util/java_util_arraydeque.htm)<br><br>ArrayDeque class provides resizable-array and implements the Deque interface. Array deques have no capacity restrictions so they grow as necessary to support usage.|
|9|[EnumMap](https://www.tutorialspoint.com/java/util/java_util_enummap.htm)<br><br>EnumMap class is a specialized Map implementation for use with enum keys. All of the keys in an enum map must come from a single enum type that is specified, explicitly or implicitly, when the map is created.|
|10|[Queue](https://www.tutorialspoint.com/java/java_util_queue.htm)<br><br>The queue interface is provided in java.util package and it implements the Collection interface. The queue implements FIFO i.e. First In First Out. This means that the elements entered first are the ones that are deleted first.|
|11|[Deque](https://www.tutorialspoint.com/java/util/java_util_deque.htm)<br><br>EnumMap class is a specialized Map implementation for use with enum keys. All of the keys in an enum map must come from a single enum type that is specified, explicitly or implicitly, when the map is created.|

![Ezoic](https://go.ezodn.com/utilcave_com/ezoicbwa.png "ezoic")

## The Collection Algorithms

The collections framework defines several algorithms that can be applied to collections and maps. These algorithms are defined as static methods within the Collections class.

Several of the methods can throw a **ClassCastException**, which occurs when an attempt is made to compare incompatible types, or an **UnsupportedOperationException**, which occurs when an attempt is made to modify an unmodifiable collection.

Collections define three static variables: EMPTY_SET, EMPTY_LIST, and EMPTY_MAP. All are immutable.

|Sr.No.|Algorithm & Description|
|---|---|
|1|[The Collection Algorithms](https://www.tutorialspoint.com/java/java_collection_algorithms.htm)<br><br>Here is a list of all the algorithm implementation.|

### How to Use an Iterator?

Often, you will want to cycle through the elements in a collection. For example, you might want to display each element.

The easiest way to do this is to employ an iterator, which is an object that implements either the Iterator or the ListIterator interface.

Iterator enables you to cycle through a collection, obtaining or removing elements. ListIterator extends Iterator to allow bidirectional traversal of a list and the modification of elements.

|Sr.No.|Iterator Method & Description|
|---|---|
|1|[Using Java Iterator](https://www.tutorialspoint.com/java/java_using_iterator.htm)<br><br>Here is a list of all the methods with examples provided by Iterator and ListIterator interfaces.|

### How to Use a Comparator?

Both TreeSet and TreeMap store elements in a sorted order. However, it is the comparator that defines precisely what _sorted order_ means.

This interface lets us sort a given collection any number of different ways. Also this interface can be used to sort any instances of any class (even classes we cannot modify).

|Sr.No.|Iterator Method & Description|
|---|---|
|1|[Using Java Comparator](https://www.tutorialspoint.com/java/java_using_comparator.htm)<br><br>Here is a list of all the methods with examples provided by Comparator Interface.|

### How to Use a Comparable?

Both TreeSet and TreeMap store elements in a sorted order. We can use Comparable interface that defines precisely what _sorted order_ means.

This interface lets us sort a given collection any number of different ways. Also this interface can be used to sort any instances of any class (even classes we cannot modify).

|Sr.No.|Iterator Method & Description|
|---|---|
|1|[Using Java Comparable](https://www.tutorialspoint.com/java/java_using_comparable.htm)<br><br>Here is a list of all the methods with examples provided by Comparable Interface.|

## Summary

The Java collections framework gives the programmer access to prepackaged data structures as well as to algorithms for manipulating them.

A collection is an object that can hold references to other objects. The collection interfaces declare the operations that can be performed on each type of collection.

The classes and interfaces of the collections framework are in package java.util.
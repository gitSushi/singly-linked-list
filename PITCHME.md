@snap[midpoint span-100]
# Singly Linked List
@snapend

@snap[north span-100 fragment]
## **Data Structure**
@snapend

+++

@title[Properties]

@snap[north-west span-70 text-center my-orange-text]
#### About the singly linked list
@snapend

@snap[my-orange-strong]
@ul[list-spaced-bullets text-09]
- The singly linked list is the simplest list amongst the linked list.
- It starts with only one node, the head which is set to null.
- It points to the next node, which will allow to traverse the list only from the head node to the end of the list.
- Let's have a look at the **code**.
@ulend
@snapend

+++

@snap[my-orange-text]
### The details of the code
@snapend

+++?gist=gitSushi/6e80057358793b4ab282d7adb68d1171
@title[Code review]

@snap[north span-100 my-orange-text text-10]
@[1-6](Instead of using a class which is essentially a function returning an object, we will do just that to declare our function *Node*.)
@[8-10](*SinglyLinkedList* will be the outer function of our closures. Initialization of the two variables that we need to keep track of: *head* and *length* of the list.)
@[12-14](A helper function that returns a boolean wether the list empty or not.)
@[16-28](append)
@[30-40](prepend)
@[42,](Declare the insertValueAtIndex with its two parameter, value, index.)
@[43-44](If the index is out of bounds log "Invalid index".)
@[45-47](Call the prepend function if the index is 0.)
@[48-52](Knowing the index is valid, initialize the necessary variables to insert the new node. The *previousNode* will allow to point at the new node which will point at the *currentNode*.)
@[53-57](Iterate till the index is found which sets the variables.)
@[58-63](Finally add the new node by referencing the pointers. Finally increment length.)
@snapend

+++?image=assets/img/code.jpg&opacity=60&position=left&size=45% 100%

@snap[east span-50 text-center]
## Happy **coding** !!
@snapend

@snap[south-east span-50 text-center text-06]
[Edit on Codepen @fa[external-link]](https://codepen.io/gitsushi/pen/xxVBOxN/right?editors=0012)
@snapend

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
@transition[slide]

@snap[north span-100 my-orange-text text-10]
@[1-6](Instead of using a class which is essentially a function returning an object, we will do just that to declare our function *Node*.)
@[8-10](*SinglyLinkedList* will be the outer function of our closures. We initialize the two variables that we need to keep track of : *head* and *length* of the list.)
@[12-14](A helper function that returns a boolean wether the list empty or not.)
@[16-19](The *append* function references an instance of the node object then if the list is empty saves the node as the *head* of the list)
@[20-28](Starting from the *head* we iterate until a node that points to *null* is found. It will be set as the new node. *length* is incremented.)
@[30-40](The *prepend* function is very similar to the append function. In the second part (from *else*), the current head will become the new *head*'s pointer.)
@[42,](The *insertValueAtIndex* function is a little more complex with its two parameters : *value*, *index*.)
@[43-44](If the *index* is out of bounds log "Invalid index".)
@[45-47](Invoke the prepend function if the *index* is 0.)
@[48-52](Knowing the index is valid, initialize the necessary variables to insert the new node. In this order, the *previousNode* will point at the new **node** which will point at the *currentNode*.)
@[53-57](Iterate until the *index* is found which sets the variables.)
@[58-63](Add the new node by referencing the pointers. Finally increment *length*.)
@[65-67](The *showList* function will first check if the list is empty and log so...)
@[68-77](or traverse the list, save the values in an array then log the result in the form of a string with separators.)
@[79-81](The *showLength* function is quite self-explanatory. It will log the *length* of our list.)
@snapend

+++?image=assets/img/linked_list_1.png&opacity=60&position=left&size=45% 100%

@snap[east span-50 text-center]
## Happy **coding** !!
@snapend

@snap[south-east span-50 text-center text-06]
[Edit on Codepen @fa[external-link]](https://codepen.io/gitsushi/pen/xxVBOxN/right?editors=0012)
@snapend

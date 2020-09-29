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
@[83-85](The *deleteAtIndex* function first checks if the list is empty or the *index* is out of bounds.)
@[86-89](If the *index* is 0 the second node becomes the new *head*.)
@[90-93](The *previousNode*'s pointer will become the *currentNode*'s pointer as to skip the *currentNode* thus deleting it.)
@[94-104](Iterate to find the *currentNode* corresponding to the index. Make the changes and decrement *length*. Optionally one can return the resulting list.)
@[106-108](The *deleteAtValue* function starts with returning *null* if the list is empty.)
@[109-117](We traverse the list (in a similar previous way) and look for the value. The use of a *counter* will become apparent in the following part.)
@[118-128](If the value isn't found, the function returns *null*. If the counter is 0 the second node becomes the *head* else the node to delete is skipped and *length* is decreased.)
@[130-139](Eventually the closures are returned in an object. (Using the object property initializer syntax of ES6))
@[141-151](All that is left is to create an instance of the *SinglyLinkedList* and invoke its closures.)
@snapend

+++?image=assets/img/linked_list_1.png&opacity=60&position=left&size=45% 100%

@snap[east span-50 text-center]
## Happy **coding** !!
@snapend

@snap[south-east span-50 text-center text-06]
[Edit on Codepen @fa[external-link]](https://codepen.io/gitsushi/pen/xxVBOxN/right?editors=0012)
@snapend

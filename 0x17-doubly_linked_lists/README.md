This repository contains a collection of functions. Below is a brief description of each task.

## Linked List Functions

1. **print_dlistint(const dlistint_t *h)**:
   - Prints all the elements of a `dlistint_t` linked list.
   - Returns the number of nodes.
   
2. **dlistint_len(const dlistint_t *h)**:
   - Returns the number of elements in a linked `dlistint_t` list.
   
3. **add_dnodeint(dlistint_t **head, const int n)**:
   - Adds a new node at the beginning of a `dlistint_t` list.
   - Returns the address of the new element, or NULL if it failed.
   
4. **add_dnodeint_end(dlistint_t **head, const int n)**:
   - Adds a new node at the end of a `dlistint_t` list.
   - Returns the address of the new element, or NULL if it failed.
   
5. **free_dlistint(dlistint_t *head)**:
   - Frees a `dlistint_t` list.
   
6. **get_dnodeint_at_index(dlistint_t *head, unsigned int index)**:
   - Returns the nth node of a `dlistint_t` linked list.
   - Returns NULL if the node does not exist.
   
7. **sum_dlistint(dlistint_t *head)**:
   - Returns the sum of all the data (n) of a `dlistint_t` linked list.
   - Returns 0 if the list is empty.
   
8. **insert_dnodeint_at_index(dlistint_t **h, unsigned int idx, int n)**:
   - Inserts a new node at a given position in a `dlistint_t` list.
   - Returns the address of the new node, or NULL if it failed.
   
9. **delete_dnodeint_at_index(dlistint_t **head, unsigned int index)**:
   - Deletes the node at index `index` of a `dlistint_t` linked list.
   - Returns 1 if it succeeded, -1 if it failed.

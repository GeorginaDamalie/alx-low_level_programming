Linked List Functions:

1. `size_t print_list(const list_t *h);`
   - Prints all the elements of a linked list_t list.
   - Format: Each element on a new line.
   - If str is NULL, it prints `[0] (nil)`.
   - Returns the number of nodes in the list.

2. `size_t list_len(const list_t *h);`
   - Returns the number of elements in a linked list_t list.

3. `list_t *add_node(list_t **head, const char *str);`
   - Adds a new node at the beginning of the linked list_t list.
   - Returns the address of the new element or NULL if it fails.
   - str needs to be duplicated.

4. `list_t *add_node_end(list_t **head, const char *str);`
   - Adds a new node at the end of the linked list_t list.
   - Returns the address of the new element or NULL if it fails.
   - str needs to be duplicated.

5. `void free_list(list_t *head);`
   - Frees the memory allocated for a linked list_t list.



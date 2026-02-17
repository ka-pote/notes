# Recap
## 2D array

### Pass by Reference
## S T R I N G S !
## Dynamic Memory Allocation
In languages like C, you need your memory to expand, you're going to need dynamic allocation. (standard)C in particular, uses malloc and calloc.


### Malloc
Note: pointer asterisk can be after data type or variable name. I prefer the former


`(data type)* a = malloc(size, preferably "items * sizeof(type)) )` (It's recommended in C99+ to **_not_** cast malloc)  

E.g.,
```
int n = 10;
int* a = (int *)malloc(n * sizeof(int))
```
Q: Why sizeof and n?
A1: While you can use just the size as-is, it's not practical because you might stumble in 32-bit, heck even 16-bit systems. And different architecture and bus size == different size of these variables.
A2: We used n so we don't lose track of how large it is because C doesn't have a way to size dynamic array— pointers have always the same size since well, they just point to address.
### Calloc
Malloc don't initialize so what happens is that you fetch gibberish from memory. Calloc initialize to 0.
#### Syntax
```
(type)* a = (type *)calloc(count , size)
```

E.g.,

```
int* a= (int *)calloc(n, sizeof(int))
```



### Realloc
Say, you want a resize (shrink or expand)
#### Syntax:
```
int* [New pointer] = (int *)realloc([pointer you wanna change], [new size])
```
E.g., 
```
int* b = (int *) realloc(a, (n+10) * sizeof(int) )
```

---

Note: It's a good idea when dynamically allocating to check if it's successful (i.e., not NULL) so we don't write to a NULL pointer and boom.

### Free
Free deallocates the memory for later use. If you forget to, it will stay in memory til you restart so don't.
#### Syntax
```
free(a)
a = NULL

```
It's nice to Null your dyalloced pointer so it doesn't point to something

# Abstract Data Type
A user-defined data type. It's composed of two parts:
1. Data declaration 
2. Operation declaration
E.g.,: Linked list, queue, tree
## Self-referential Structures
Contains a pointer that points to a struct of same struct type

E.g.,:
```
typedef struct{
char name[20];
int x;
student* n;
};
```

# Linked List
```
typedef struct{
int x;
node* next;
}node;
```
![[Linked_list]]
## Creating node
```
current = head;
n -> x = 25;
n -> next = NULL;
```
## E.g.,
![[ITE14-Data_Structures_And_Algorithms 2026-02-03 09.18.12.excalidraw]]

```c
typedef struct list{
int x;
struct list* next;
}list;

list* add(){
list n = malloc(sizeof(list));
puts("int. iykyk");
_sf("%d", &n->x);
n->next=NULL;

return n;
}



main(){
list* n1 = malloc(sizeof(list));
n1->x=5; n1->next=NULL;
list* n4 = add();
n3->next = n4;

list *head, *current;
head = n1;
current = head;

_w(curren != NULL){
	_pf("%d", current->x);
	current=current->next;	
	}
_r 0;
}
```

## Doubly Linked List
![[ITE14-Data_Structures_And_Algorithms 2026-02-09 15.37.44.excalidraw]]
**Pros**
- no need for second var 
**Cons**
- more space (2 pointers)
- more operations/statements
```c
typedef struct list{
int x;
struct list *left;
struct list *right;
}list;
```

```c
//node deletion in single ll iirc
current = head;
prev = NULL;
while(current != NULL){
	if(current->next == NULL){
	prev->next = NULL;
	free(current);
	current = NULL;
	}
	prev = current;
	current = current->next
}

```

## Circular Linked List
![[ITE14-Data_Structures_And_Algorithms 2026-02-16 15.38.16.excalidraw]]
# Stack
![[ITE14-Data_Structures_And_Algorithms 2026-02-16 16.12.10.excalidraw]]
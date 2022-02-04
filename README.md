# making and accessing linked-lists

struct s_list
{ 
  int   i;
  char  c;
  struct s_list *next;
  };
  
  int main(void)
  {
    struct s_list elem1;
    struct s_list elem2;
    struct s_list elem3;
    struct s_list *begin;
    
    begin = &elem1;
    elem1.next = &elem2;
    elem2.next = &elem3;
    elem3.next = 0;
    
    elem1.i = 98;
    elem2.i = 109;
    elem3.i =42;
    
    printf("%d\n", begin->i);
    printf("%d\n", begin->next->i);
    printf("%d\n" begin->next->next->i);
    }
    
    gcc main.c &&./a.out
    98
    109
    42

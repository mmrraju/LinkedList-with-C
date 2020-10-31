//C Program to push value in Linked list.
//Author MMR Raju 31-10-2020

#include<stdio.h>
#include<stdlib.h>
struct Node
{
    int data;
    struct Node *next;
};
void push(struct Node** head_ref, int new_data)
{
    struct Node* new_node=(struct Node*)malloc(sizeof(struct Node));
    new_node->data=new_data;
    new_node->next= *head_ref;
    *head_ref=new_node;
}
void printList(struct Node *n)
{
    while(n!=NULL)
    {
        printf("%d ",n->data);
        n=n->next;
    }
}
int main()
{
    struct Node* head=NULL;
    push(&head, 7);
    push(&head, 3);
    push(&head, 1);
    push(&head, 2);
    push(&head, 8);
    printList(head);
}



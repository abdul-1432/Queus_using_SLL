// program for implementation of Queue USING single linked list

#include <stdio.h>
#include <stdlib.h>
struct node
{
	int data;
	struct node *link;
};
struct node *first, *neu, *temp;

void create_node();
void display_list();
void insert_end();
void delete_beginning();

void create_node()
{
	neu = (struct node *) malloc(sizeof(struct node));
	printf("enter data ");
	scanf("%d",&neu->data);
	neu->link=NULL;
}

void display_list()
{
	if (first==NULL)    // checking for underflow (empty list)
	{
		printf("List is underflow...no nodes to display");
	}
	else
	{
		printf("\n Linked List values are\n");
		temp=first;
		while(temp!=NULL)
		{
			printf("\t%u(%d,%u)",temp,temp->data,temp->link);
			temp=temp->link;    // to move to next node
		}
/*		printf("\n Linked List values are \n");
		for(temp=first;temp!=NULL;temp=temp->link)
			printf("\t%d",temp->data);   */
	}
}

void insert_end()
{
	create_node();
	if (first==NULL)  // if list id empty
	{
		first=neu;
	}
	else
	{
		temp=first;
		while(temp->link!=NULL)  // is it the last node?
		{
			temp=temp->link;  // to move to next node
		}
		temp->link=neu;
	}
}
	
void delete_beginning()
{
	if (first==NULL)
		printf("list is empty...no nodes to delete");
	else
	{
		neu=first;			// denote the first node as neu
		first=first->link;  // move first to next node
		neu->link=NULL;     // break the link of neu
		printf("\n %d is being delete",neu->data);  // showing data that is getting removed
		free(neu);			// deallocate memory of neu
		neu=NULL;           // replace address of neu with NULL
	}
}

void main()
{
	int cho;
	neu=first=temp=NULL;
	do
	{
		printf("\n\n*** Queue Operations USING Single Linked List ***");
		printf("\n 1 Enqueue");
		printf("\n 2 Dequeue");
		printf("\n 3 List the nodes");
		printf("\n 4 Exit");
		printf("\n Enter your choice (1-4) : ");
		scanf("%d",&cho);
		if (cho==1)
			insert_end();
		else if (cho==2)
			delete_beginning();
		else if (cho==3)
			display_list();
		else if (cho==4)
			printf("\n Thank you");
		else
			printf("Invalid choice...retry");
	}while(cho!=4);
	printf("\n* * * End of Program * * *");
}

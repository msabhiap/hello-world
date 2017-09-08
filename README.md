# hello-world

#include<stdio.h>
#include<conio.h>
#include<stdlib.h>

struct node
  {
  int info;
  struct node *next, *prev;
  };
  typedef struct node node;

void linearprobing(int a[],int n);
void qudraticprobing(int a[],int n);
void chaining (node *[],int);
 void main()
 {


     while(1){
     	printf("\nWhat do you want to do?\n");
      printf("\n 1. Insert data");
      printf("\n 2. qudaratic");
      printf("\n 3. chaining");
      printf("\n 4. Delete");
      printf("\n 5. Exit\n");

      scanf("%d", &n);
      switch(n){
      	case 1:
				 printf("\n Enter data to insert at beginning");
             scanf("%d", &item);
             insert(&root, item);
             break;
			case 2:
         	printf("\n Enter data");
            scanf("%d", &item);
            bsearch(root, item);
         break;
         case 3:
         printf("\n Enter data");
            scanf("%d", &item);
            bsearch(root, item);
         printf("\n
         case 4:
         	printf("\n Enter data you want to delete");
            scanf("%d", &item);
         	del(&root,item);
         	break;
         case 5:
         	exit(0);
         break;
         default:
         	printf("Invalid entry");
          }
     }

}
 	int a[10],i,data,ch,n;
   node *b[10];
   for(i=0;i<10;i++)
   {
   	a[i]=-1;
      b[i]=NULL;
   }
   printf("enter no of elements\n");
   scanf("%d",&n);
   chaining(b,n);
   getch();
 }

 void linearprobing(int a[],int n)
 	{
   	int i,key,h,j;
      for(i=0;i<n;i++)
      	{
         	printf("enter data");
            scanf("%d",&key);
            j=0;
            while(1)
            	{
               	h=((key%10)+j)%10;
                  if(a[h]==-1)
                  	{
                     	a[h]=key;
                        break;
                     }
                     j++;
                  }
               }
               printf("\n the data in hash table:");
               for(i=0;i<10;i++)
               {
               	if(a[i]!=-1)
                  {
                  	printf("\n a[%d]=%d",i,a[i]);
                  }
               }
            }



      void qdraticprobing(int a[],int n)
      {
      	int i,key,h,j;
         for(i=0;i<n;i++)
         {
         	printf("\nenter the data");
            scanf("%d",&key);
            j=0;
            while(1)
            {
            	h=((key%10)+(j*j))%10;
               if(a[h]==-1)
               {
               	a[h]=key;
                  break;
               }
               j++;
            }
         }
         printf("\nthe dat in hash table:");
         for(i=0;i<10;i++)
         {
         	if(a[i]!=-1)
            {
            	printf("\n a[%d]=%d",i,a[i]);
            }
         }
      }

      void chaining (node *b[],int n)
      {
      	node *temp;
         int i,key,h;
         for(i=0;i<n;i++)
 				{
            	printf("enter data\n");
               scanf("%d",&key);
               h=key%10;
               temp=(node *)malloc(sizeof(node));
               temp->info=key;
               temp->next=b[h];
               b[h]=temp;
            }

            node *temp1;
            for(i=0;i<10;i++)
            {
            	temp=b[i];
               if(temp!=NULL)
               {
               	temp=b[i];
                  if(temp!=NULL)
                  {
                  	printf("\n b[%d]=%d",i,temp->info);
                     temp1=temp->next;
                  while(temp1!=NULL){
                  	printf("\n b[%d]=%d",i,temp->info);
                     temp1=temp1->next;
                     }
                  }
               }
            }
            }

